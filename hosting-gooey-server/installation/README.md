---
icon: download
description: >-
  Choose an installation path, understand what gets installed, and verify the
  result.
---

# Installation Guide

A step-by-step guide to getting Gooey Server running on your own machine.

Before you invest the time: for most developers we **do not** recommend running or forking Gooey Server — use the [API](https://gooey.ai/api/) or the [Python SDK](https://github.com/GooeyAI/python-sdk) instead. Install locally if you want to build a new recipe, add an unsupported AI model, run your own server cluster, or meet enterprise data requirements. See [What is Gooey Server?](../) for the full rationale.

## Choose your path

|                     | **Quickstart with Docker**                                             | **Manual Installation**                            |
| ------------------- | ---------------------------------------------------------------------- | -------------------------------------------------- |
| **Setup time**      | ~10 min (mostly the first build)                                       | ~45 min                                            |
| **Platforms**       | macOS, Linux, Windows                                                  | macOS, Linux                                       |
| **Recipe coverage** | All except recipes needing playwright or mediapipe                     | Everything                                         |
| **Best for**        | Trying Gooey out, running it as a self-hosted service, backend work    | Day-to-day development, debugging individual services |

{% hint style="success" %}
**Start with [Quickstart with Docker](quickstart-with-docker.md).** Switch to [Manual Installation](manual-installation.md) when you need full recipe parity or a faster edit-run loop. The two paths share the same ports and credentials, so you can also run the backing services from Docker Compose while running the app processes natively.
{% endhint %}

<table data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h4>Quickstart with Docker</h4></td><td>One command brings up the whole stack. Recommended starting point.</td><td><a href="quickstart-with-docker.md">quickstart-with-docker.md</a></td></tr><tr><td><h4>Manual Installation</h4></td><td>Everything runs natively. Full recipe coverage, easier debugging.</td><td><a href="manual-installation.md">manual-installation.md</a></td></tr></tbody></table>

## What gets installed

Four app processes on top of four backing services:

| Component                                | What it does                                                                                                            | Port   |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------ |
| gooey-gui (`gooey-gui/`)                 | Remix/React frontend. Asks the Python server to render each page as a JSON component tree and subscribes to Redis pub/sub for live updates | `3000` |
| Python API + GUI Server (`server.py`)    | FastAPI app serving the public API and the page-render endpoints                                                        | `8080` |
| Celery workers (`celeryapp/`)            | Run the actual recipes: pull jobs from RabbitMQ, call model providers, save results                                     | —      |
| Django Admin (`gooeysite/`)              | Admin UI over the same Postgres database                                                                                | `8000` |
| PostgreSQL 15                            | Application database                                                                                                    | `5432` |
| Redis 8                                  | Cache + realtime pub/sub                                                                                                | `6379` |
| RabbitMQ                                 | Celery broker                                                                                                           | `5672` |
| Vespa                                    | Vector + full-text search (doc search / RAG)                                                                            | `8085` |

See the [architecture diagram](../#architecture) for how they connect.

{% hint style="info" %}
**No cloud account is required.** A default install authenticates with local Django email/password (Firebase auth is off unless you set `ENABLE_FIREBASE_AUTH`), stores uploads on the local filesystem (Google Cloud Storage is off unless you set `GS_BUCKET_NAME`), and leaves payments, analytics, cloud moderation, and managed secrets disabled. All four backing services are open source. See [Platform Independence](../platform-independence.md) for the full accounting.
{% endhint %}

## Optional add-ons

Everything here is opt-in — skip it until you need the feature.

### Provider API keys

Each model provider becomes usable once its key is in `.env`; on the Docker path the app services read the same root `.env`, so add keys there and restart. `COMPOSIO_API_KEY` enables the Composio tools selector. Bot deployments need `FB_APP_ID` / `TWILIO_ACCOUNT_SID` / `SLACK_CLIENT_ID` — the deploy buttons stay hidden and creation is blocked until they're set. Full list: [Configuration Reference](../configuration.md).

### Functions runtime (Cloudflare Workers)

The Functions recipe executes user-supplied JavaScript in sandboxed [Cloudflare Dynamic Workers](https://developers.cloudflare.com/dynamic-workers/) via `functions/executor_cf/`. Run it locally with wrangler:

```bash
cd functions/executor_cf
npm install
npx wrangler dev
```

Then point Gooey at it in `.env`:

```env
CF_FUNCTIONS_URL=http://localhost:8787
```

To deploy it to Cloudflare instead, see [`functions/executor_cf/wrangler.jsonc`](https://github.com/GooeyAI/gooey-server/blob/master/functions/executor_cf/wrangler.jsonc).

### Secret scanning

Gitleaks runs pre-commit (see `.pre-commit-config.yaml`). Test it without committing by running `pre-commit`. Prefer labelling false positives with a `#gitleaks:allow` comment over skipping with `SKIP=gitleaks git commit`.

### Code formatting

This project uses [ruff](https://docs.astral.sh/ruff/).

## Keeping your install up to date

After a `git pull`, three kinds of change need action:

```bash
git pull

# new/changed Python or Node dependencies (pyproject.toml, poetry.lock, package.json)
poetry install --with dev                                    # Manual install
docker compose -f docker-compose.local.yml up --build        # Docker

# new database migrations
./manage.py migrate                                          # Manual install
docker compose -f docker-compose.local.yml run --rm admin ./manage.py migrate   # Docker

# changed Vespa schema
./manage.py runscript setup_vespa_db
```

On the Docker path the `admin` service applies migrations on every start, so a plain `up` usually covers it. On the manual path nothing is automatic — and remember the Celery worker needs a manual restart to pick up any code change.

## Verifying your install

Work through this once:

* [ ] [http://localhost:3000/explore](http://localhost:3000/explore) lists workflows
* [ ] [http://localhost:8080/docs](http://localhost:8080/docs) renders the API reference
* [ ] [http://localhost:8000](http://localhost:8000) accepts your Django admin login
* [ ] You can log in at [http://localhost:3000/login/](http://localhost:3000/login/) with your own email
* [ ] Your workspace has a non-zero balance in the admin
* [ ] A recipe run completes — pick a simple one, hit Run, and watch the Celery logs

Then run the test suite:

```bash
ulimit -n unlimited   # raise the open-file limit
./scripts/run-tests.sh
```

The script downloads `fixture.json`, checks formatting with `ruff format --diff`, and runs pytest. Extra arguments are passed through to pytest, e.g. `./scripts/run-tests.sh -k asr`.

## Troubleshooting

<details>

<summary>The first Docker build is very slow</summary>

Expected — it installs the full Python dependency set and builds the frontend. Later builds hit the layer cache. On Apple Silicon, OrbStack builds native arm64 and is noticeably faster than Docker Desktop.

</details>

<details>

<summary>A recipe fails with an insufficient-credits error</summary>

Your workspace balance is 0. Top it up at [http://localhost:8000/workspaces/workspace/](http://localhost:8000/workspaces/workspace/).

</details>

<details>

<summary>A recipe fails with an authentication or API-key error</summary>

You picked a cloud-hosted model. Either add that provider's key to `.env` and restart, or [register a local model](../adding-local-ai-models.md).

</details>

<details>

<summary>Migrations ran but my data isn't in Postgres</summary>

On the manual path, missing `PG*` variables make Django fall back to `db.sqlite3` in the repo root. Fill in `.env` per [step 4 of the manual install](manual-installation.md#4-configure-env) and re-run `./manage.py migrate`.

</details>

<details>

<summary>Doc search / RAG recipes error out</summary>

Vespa isn't running or its schema was never applied. Check that the container is up, then run `./manage.py runscript setup_vespa_db`.

</details>

<details>

<summary>Recipes hang as "queued" forever</summary>

The Celery worker isn't running, or it can't reach RabbitMQ. Check its logs — on the Docker path, `docker compose -f docker-compose.local.yml logs -f celery`.

</details>

<details>

<summary>Code changes don't take effect</summary>

The Celery worker never picks up code changes on its own — restart it. On the Docker path, frontend changes require a rebuild (`up --build`).

</details>

<details>

<summary><code>localhost:3000</code> is flaky on macOS</summary>

Under OrbStack, use `https://ui.gooey-server.orb.local` instead.

</details>

<details>

<summary>Some recipe complains about playwright or mediapipe</summary>

You're on the Docker path; `Dockerfile.local` omits both. Use [Manual Installation](manual-installation.md) for those recipes.

</details>

<details>

<summary>Something in the Docker stack is wedged</summary>

Rebuild from scratch with `docker compose -f docker-compose.local.yml build --no-cache`. Only resort to `down -v` if you're willing to lose your local database.

</details>

---

Still stuck? Ask in [Discord](https://gooey.ai/discord).
