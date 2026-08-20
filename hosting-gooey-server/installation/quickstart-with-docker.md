---
icon: bolt
description: >-
  Bring up Postgres, Redis, RabbitMQ, Vespa and all four app services with a
  single Docker Compose command.
---

# Quickstart with Docker

The fastest way to run Gooey Server. One command starts Postgres, Redis, RabbitMQ, Vespa, and all four app services.

**Setup time:** ~10 minutes, mostly the first build · **Platforms:** macOS, Linux, Windows

{% hint style="info" %}
`Dockerfile.local` is a deliberately lightweight image. A few recipes that depend on playwright or mediapipe won't work in-container — see [Known limitations](#known-limitations) below. For full recipe parity, use [Manual Installation](manual-installation.md).
{% endhint %}

## 1. Install Docker

{% tabs %}
{% tab title="macOS" %}
Install [OrbStack](https://orbstack.dev/download). Recommended on Apple Silicon: native arm64, fast builds.

{% hint style="warning" %}
OrbStack requires you to launch it manually the first time.
{% endhint %}
{% endtab %}

{% tab title="Linux" %}
Install [Docker Engine](https://docs.docker.com/engine/install/) and the [Compose plugin](https://docs.docker.com/compose/install/linux/).
{% endtab %}

{% tab title="Windows" %}
Install [Docker Desktop](https://docs.docker.com/desktop/setup/install/windows-install/).
{% endtab %}
{% endtabs %}

## 2. Clone the repo

```bash
git clone https://github.com/GooeyAI/gooey-server.git
cd gooey-server
```

The frontend lives at `gooey-gui/` inside this repo — there are no submodules to initialize.

## 3. Start the stack

```bash
docker compose -f docker-compose.local.yml up --build
```

The first build takes a few minutes. Leave this terminal running (or add `-d` to detach). Database migrations and the Vespa schema are applied automatically by the `admin` service on startup.

Once it's up:

| Service             | URL                                                              |
| ------------------- | ---------------------------------------------------------------- |
| UI                  | [http://localhost:3000/explore](http://localhost:3000/explore)   |
| API docs            | [http://localhost:8080/docs](http://localhost:8080/docs)         |
| Django admin        | [http://localhost:8000](http://localhost:8000)                   |
| RabbitMQ management | [http://localhost:15672](http://localhost:15672)                 |

{% hint style="info" %}
On OrbStack, services are also reachable at `https://<service>.gooey-server.orb.local` (e.g. [https://ui.gooey-server.orb.local](https://ui.gooey-server.orb.local)), which is often more reliable than `localhost:3000`.
{% endhint %}

## 4. Run first-time setup

Once, after the stack is up:

```bash
docker compose -f docker-compose.local.yml run --rm admin ./manage.py runscript setup_local
```

This runs migrations, seeds a starter set of LLM model specs, and creates a Django admin superuser.

Log in to [http://localhost:8000](http://localhost:8000) with username **`admin`** / password **`admin`**.

{% hint style="danger" %}
These credentials are for local development only — never expose this instance publicly as-is.
{% endhint %}

## 5. Create your app account

The Django admin user is separate from your Gooey app account. Go to [http://localhost:3000/login/](http://localhost:3000/login/) and enter any email and password: with local auth, an unknown email signs up as a new user and the password you type is set on first login.

## 6. Give your workspace credits

Recipe runs are metered against workspace credits, and a locally created account starts at **0**. Grant yourself credits in the Django admin:

1. Open [http://localhost:8000/workspaces/workspace/](http://localhost:8000/workspaces/workspace/)
2. Search for your email and open your personal workspace
3. Set **Balance** to something generous, e.g. `10000`, and save

Skip this and recipe runs will fail with an insufficient-credits error.

{% hint style="success" %}
The app links you there directly. Visit [http://localhost:3000/account/billing](http://localhost:3000/account/billing) — with no Stripe key configured, the billing page shows your balance plus an **Add balance in Django admin** link straight to your workspace's admin page. The link honours `ADMIN_BASE_URL`, which already defaults to `http://localhost:8000`.
{% endhint %}

## 7. Everyday commands

```bash
# stop everything (data is preserved)
docker compose -f docker-compose.local.yml down

# follow logs for one service
docker compose -f docker-compose.local.yml logs -f celery

# rebuild after changing pyproject.toml / package.json
docker compose -f docker-compose.local.yml up --build

# open a shell in the app image
docker compose -f docker-compose.local.yml run --rm admin bash
```

Python source is bind-mounted into the containers, so Python edits need only a restart of the affected service (`docker compose -f docker-compose.local.yml restart api celery`) — not a rebuild. Frontend changes are baked in at build time, so they do need `--build`.

{% hint style="danger" %}
`docker compose -f docker-compose.local.yml down -v` also deletes the named volumes — your database, uploads, and Vespa index are gone for good. Use it only when you want a truly clean slate, and re-run [step 4](#4-run-first-time-setup) afterwards.
{% endhint %}

## Known limitations

`Dockerfile.local` is a deliberately lightweight image: it skips compiling poppler from source, amd64-only packages, playwright, and mediapipe. A few recipes that depend on playwright or mediapipe won't work in-container. For full parity, use [Manual Installation](manual-installation.md).

## Next steps

* [Verify your install](./#verifying-your-install)
* [Add a local AI model](../adding-local-ai-models.md) so you can run recipes without any cloud API keys
* [Configuration Reference](../configuration.md) for every available setting
* [Troubleshooting](./#troubleshooting) if something isn't working
