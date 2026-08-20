---
icon: screwdriver-wrench
description: >-
  Run every service natively for full recipe coverage and easier per-service
  debugging.
---

# Manual Installation

Everything runs directly on your machine. More setup than the [Docker path](quickstart-with-docker.md), but full recipe coverage and easier per-service debugging.

**Setup time:** ~45 minutes · **Platforms:** macOS, Linux

## 1. Python and Poetry

Install [pyenv](https://github.com/pyenv/pyenv), then the same Python version as the [Dockerfile](https://github.com/GooeyAI/gooey-server/blob/master/Dockerfile) — currently **3.10.12**:

```bash
# linux, if you don't have pyenv yet
curl https://pyenv.run | bash

pyenv install 3.10.12
pyenv local 3.10.12
```

Install [Poetry](https://python-poetry.org/docs/) (on Linux it's likely in your distro's package repos), then create the virtualenv and install dependencies:

```bash
poetry shell
poetry install --with dev
```

{% hint style="info" %}
On Linux you may have to remove `package-mode = false` from line 7 of `pyproject.toml` for `poetry install` to succeed.
{% endhint %}

## 2. System packages

{% tabs %}
{% tab title="macOS" %}
```bash
brew install redis rabbitmq postgresql@15 zbar
```

Optional, for HEIC image support ([wand docs](https://docs.wand-py.org/en/0.5.7/guide/install.html)):

```bash
brew install freetype imagemagick
export MAGICK_HOME=/opt/homebrew
```
{% endtab %}

{% tab title="Linux" %}
Install `redis`, `rabbitmq-server`, `postgresql` 15, and the `zbar` library with your distro's package manager.
{% endtab %}
{% endtabs %}

## 3. Start the backing services

{% tabs %}
{% tab title="macOS" %}
```bash
brew services start redis
brew services start rabbitmq
brew services start postgresql@15
```
{% endtab %}

{% tab title="Linux" %}
```bash
sudo systemctl enable --now redis rabbitmq-server postgresql
```

Also enable password authentication for the `gooey` user. Open `pg_hba.conf` (usually `/etc/postgresql/<version>/main/` or `/var/lib/pgsql/<version>/data/`) and add these lines at the bottom:

```
local    all        gooey                    md5
host     all        gooey                    md5
```

Then `sudo systemctl restart postgresql`.
{% endtab %}
{% endtabs %}

## 4. Configure `.env`

Create a `.env` at the repo root.

{% hint style="warning" %}
This step is easy to miss and matters: **if the `PG*` variables are unset, the server silently falls back to SQLite** instead of your Postgres database.
{% endhint %}

```env
PGHOST=localhost
PGPORT=5432
PGUSER=gooey
PGPASSWORD=gooey
PGDATABASE=gooey

REDIS_URL=redis://localhost:6379
REDIS_CACHE_URL=redis://localhost:6379
LOCAL_CELERY_BROKER_URL=amqp://
```

Everything else has a working local default. See the [Configuration Reference](../configuration.md) for the full list of settings.

## 5. Initialize the database

```bash
# create the gooey user and database
./manage.py sqlcreate | psql postgres     # macOS
./manage.py sqlcreate | sudo -u postgres psql postgres    # Linux

# confirm you can connect (password: gooey)
psql -W -U gooey gooey

# apply migrations
./manage.py migrate

# create your Django admin user
./manage.py createsuperuser
```

Optionally load the sample data fixture. `fixture.json` is downloaded by `./scripts/run-tests.sh`, so run that first (or fetch the URL from the script):

```bash
./manage.py loaddata fixture.json
```

{% hint style="danger" %}
To start over from scratch: `./manage.py reset_db -c` drops the entire database. Everything in it is lost.
{% endhint %}

## 6. Vespa

Vespa runs in a container even on the native path, so you still need OrbStack or Docker Desktop.

```bash
docker volume create vespa

docker run \
  --hostname vespa-container \
  -p 8085:8080 -p 19071:19071 \
  --volume vespa:/opt/vespa/var \
  -it --rm --name vespa vespaengine/vespa
```

With the container running, apply the schema:

```bash
./manage.py runscript setup_vespa_db
```

## 7. Frontend dependencies

Node 20 is what the project's own image uses:

```bash
cd gooey-gui
npm install
```

## 8. Run the services

Open each in its own terminal so you can read and restart them independently:

| Service                 | Port   | Command                                                                                     |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------- |
| Python API + GUI Server | `8080` | `poetry run uvicorn server:app --host 127.0.0.1 --port 8080 --reload`                        |
| Node frontend           | `3000` | `cd gooey-gui/; PORT=3000 REDIS_URL=redis://localhost:6379 npm run build && npm run start`   |
| Celery (task runner)    | —      | `poetry run celery -A celeryapp worker -P threads -c 16 -l DEBUG`                            |
| Django admin            | `8000` | `poetry run python manage.py runserver 127.0.0.1:8000`                                        |
| Vespa                   | `8085` | see [step 6](#6-vespa)                                                                        |

Then create your app account and grant it credits exactly as on the Docker path — see [step 5](quickstart-with-docker.md#5-create-your-app-account) and [step 6](quickstart-with-docker.md#6-give-your-workspace-credits) there.

## Reloading on code changes

* **Python API + GUI Server** — reloads on save with `--reload`; refresh the page to see changes.
* **Celery worker** — must be restarted manually after every code change.
* **Frontend** — use `cd gooey-gui/; PORT=3000 REDIS_URL=redis://localhost:6379 npm run dev` while working on React code.
* **Hot reload for UI iteration** — `poetry run python server.py` reloads the webpage in place on code changes. Handy for fast UI work, but it uses more memory and usually OOMs after a few reloads.

## Starting everything at once (Honcho)

```bash
poetry run honcho start
```

Honcho runs the processes defined in [`Procfile`](https://github.com/GooeyAI/gooey-server/blob/master/Procfile) — comment out any you don't need.

{% hint style="warning" %}
Convenient, but it makes individual services much harder to debug. Prefer separate terminals for real work.
{% endhint %}

## Next steps

* [Verify your install](./#verifying-your-install)
* [Add a local AI model](../adding-local-ai-models.md) so you can run recipes without any cloud API keys
* [Configuration Reference](../configuration.md) for every available setting
* [Troubleshooting](./#troubleshooting) if something isn't working
