---
description: A copy-pasteable prompt that lets an AI coding agent (Claude Code, Cursor, Copilot, etc.) set up the Gooey.AI API in your project automatically.
---

# AI Coding Agent Setup

Using an AI coding agent? Paste this into it and it will fetch and follow the instructions on this page automatically:

{% code overflow="wrap" %}
```
Fetch and execute the appropriate instructions to set me up for Gooey.AI from https://docs.gooey.ai/api-reference/ai-coding-agent-setup.md
```
{% endcode %}

{% hint style="info" %}
The rest of this page **is** that prompt — written for an AI agent to read and act on. If you're a human, read on, it works just as well as a quickstart.
{% endhint %}

***

You are an AI coding assistant helping a developer integrate the **Gooey.AI API** into their project. Gooey.AI is a single API that gives access to 30+ AI recipes (workflows) spanning LLMs, RAG, speech-to-text, text-to-speech, lipsync, image generation, video generation, and a full conversational Copilot agent — all billed through one API key.

Follow the steps below. Don't just print this page back to the user — actually perform the steps in their project (create files, add env vars, write working code) and adapt the examples to whatever language/framework their project already uses.

## 1. Get an API key

1. The developer needs a Gooey.AI account and an API key. If they don't have one, ask them to create one at [https://gooey.ai/account/api-keys/](https://gooey.ai/account/api-keys/) (sign-up is free and includes trial credits).
2. Store it as an environment variable named `GOOEY_API_KEY` (e.g. in `.env`, git-ignored). **Never hardcode the key in source, never commit it, and never expose it to a browser/client bundle** — proxy calls through a backend if the caller is a frontend app.
3. Verify the key works with a zero-cost request:

{% code overflow="wrap" %}
```bash
curl https://api.gooey.ai/v1/balance/ \
  -H "Authorization: Bearer $GOOEY_API_KEY"
# -> {"balance": 12345}
```
{% endcode %}

## 2. The API contract

* **Base URL:** `https://api.gooey.ai`
* **Auth:** every request needs `Authorization: Bearer $GOOEY_API_KEY`
* **Interactive reference:** [https://api.gooey.ai/docs](https://api.gooey.ai/docs) and the raw spec at [https://api.gooey.ai/openapi.json](https://api.gooey.ai/openapi.json) — fetch the JSON spec directly for the exact request/response schema of a specific recipe rather than guessing at field names.
* **Recipe catalog / playground:** [https://gooey.ai/explore](https://gooey.ai/explore) — every recipe page has an **API** tab that generates ready-to-run curl/Python/Node snippets for that exact recipe with the exact fields the user has configured.

Every recipe is called the same way, just with a different `<slug>` and JSON body. There are two calling conventions:

### Sync — fast recipes (LLM text, TTS, etc.)

```
POST https://api.gooey.ai/v2/<slug>
```

Returns `200` with the finished result:

```json
{
  "id": "run_id",
  "url": "https://gooey.ai/<slug>/...",
  "created_at": "2026-01-01T00:00:00.000000Z",
  "output": { "...": "recipe-specific fields" }
}
```

### Async — slow recipes (video, lipsync, image gen, bulk jobs)

```
POST https://api.gooey.ai/v3/<slug>/async
```

Returns `202` immediately with a `Location` header (and `status_url` in the body). Poll `GET <status_url>` (same auth header) until `status` is `"completed"` or `"failed"`:

```json
{
  "run_id": "run_id",
  "web_url": "...",
  "created_at": "...",
  "run_time_sec": 4.2,
  "status": "completed",
  "detail": "human readable status",
  "output": { "...": "only present once status is completed" }
}
```

The sync endpoint also works for slow recipes, it just blocks until done — prefer async for anything that might take more than a few seconds.

### Uploading files

Pass a URL you already host, or POST `multipart/form-data` to `/v2/<slug>/form` (or `/v3/<slug>/async/form`): send the other fields as a single `json` form field, and each file under its own field name. Gooey uploads the files for you and substitutes their URLs into the request.

### Errors

See the full [Error Codes](error-codes.md) and [Rate Limits](rate-limits.md) guides. The short version: `401`/`403` = bad or missing key, `402` = out of credits, `429` = rate limited (back off and retry), `500` = the recipe run itself failed (see `detail.error`).

## 3. Popular recipe slugs

| Slug                              | What it does                                                                                        |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `agent`                             | Copilot — conversational agent with knowledge base, tools, voice & vision (`input_prompt`, `input_audio`, `input_images`, `messages`) |
| `compare-large-language-models`    | Run a prompt across one or more LLMs (`input_prompt`, `selected_models`)                            |
| `doc-search`                       | RAG: search + LLM answer over your documents                                                        |
| `doc-summary`                      | Summarize documents                                                                                  |
| `functions`                        | Run sandboxed JS/Python as a step in a pipeline                                                      |
| `speech`                           | Speech-to-text + translation (`documents`: audio/video URLs)                                        |
| `compare-text-to-speech-engines`   | Text-to-speech across providers (`text_prompt`, `tts_provider`)                                      |
| `lipsync-maker`                    | Lipsync a video/image to an audio/text track                                                         |
| `compare-ai-image-generators`      | Text-to-image across providers (`text_prompt`)                                                       |
| `video`                            | Text/image-to-video generation (`selected_models`, `inputs`)                                        |
| `qr-code`                          | AI-art QR codes                                                                                       |
| `bulk`                             | Run any recipe over every row of a spreadsheet                                                       |

Fetch `https://api.gooey.ai/openapi.json` and look up `/v2/<slug>` under `paths` for the full field list of any recipe, including enum values for fields like `selected_models` or `tts_provider`.

## 4. Example calls

Adapt these to the developer's stack — no SDK install is required, just `requests` in Python or `fetch` in Node.

**Ask an LLM something (sync):**

{% tabs %}
{% tab title="curl" %}
```bash
curl https://api.gooey.ai/v2/compare-large-language-models \
  -H "Authorization: Bearer $GOOEY_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "input_prompt": "Write a haiku about the ocean.",
    "selected_models": ["claude_sonnet_5"]
  }'
```
{% endtab %}

{% tab title="python" %}
```python
import os, requests

response = requests.post(
    "https://api.gooey.ai/v2/compare-large-language-models",
    headers={"Authorization": "Bearer " + os.environ["GOOEY_API_KEY"]},
    json={
        "input_prompt": "Write a haiku about the ocean.",
        "selected_models": ["claude_sonnet_5"],
    },
)
response.raise_for_status()
result = response.json()
print(result["output"]["output_text"])  # {"claude_sonnet_5": ["..."]}
```
{% endtab %}
{% endtabs %}

**Talk to a Copilot agent (sync):**

```python
response = requests.post(
    "https://api.gooey.ai/v2/agent",
    headers={"Authorization": "Bearer " + os.environ["GOOEY_API_KEY"]},
    json={"input_prompt": "Hello, who are you?"},
)
print(response.json()["output"]["output_text"])
```

**Generate an image and poll for it (async):**

```python
import os, time, requests

response = requests.post(
    "https://api.gooey.ai/v3/compare-ai-image-generators/async",
    headers={"Authorization": "Bearer " + os.environ["GOOEY_API_KEY"]},
    json={"text_prompt": "a synthwave sunset over mountains"},
)
response.raise_for_status()
status_url = response.json()["status_url"]

while True:
    r = requests.get(status_url, headers={"Authorization": "Bearer " + os.environ["GOOEY_API_KEY"]})
    result = r.json()
    if result["status"] in ("completed", "failed"):
        print(result)
        break
    time.sleep(3)
```

## 5. Advanced: streaming Copilot responses

If the developer has already deployed a Copilot agent (via the Gooey.AI Integrations tab) and wants to stream its replies token-by-token into their own app — see the [Getting Started](getting-started.md#quickstart) streaming example. This specific endpoint needs no `GOOEY_API_KEY` and is safe to call from a browser:

```
POST https://api.gooey.ai/v3/integrations/stream/
Body: {"integration_id": "<from the Integrations tab>", "input_prompt": "Hello, world!"}
```

The response's `Location` header (and JSON `stream_url`) is a Server-Sent Events URL — open it with `EventSource` and handle messages until `{"type": "final_response"}`.

## 6. Reference

* Interactive API docs: [https://api.gooey.ai/docs](https://api.gooey.ai/docs)
* OpenAPI spec: [https://api.gooey.ai/openapi.json](https://api.gooey.ai/openapi.json)
* Explore all recipes (with a live API code generator per recipe): [https://gooey.ai/explore](https://gooey.ai/explore)
* [Rate Limits](rate-limits.md) · [Error Codes](error-codes.md)
* Manage API keys / billing: [https://gooey.ai/account/api-keys/](https://gooey.ai/account/api-keys/)
* Support: [support@gooey.ai](mailto:support@gooey.ai)
