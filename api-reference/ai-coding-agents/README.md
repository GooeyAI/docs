---
description: Connect an AI coding agent (Claude Code, Cursor, Copilot, etc.) to the Gooey.AI API and have it wire up the integration for you.
---

# 🧑‍💻 AI Coding Agents

## What is this?

If you build with an AI coding agent — Claude Code, Cursor, GitHub Copilot, Windsurf, or similar — you can point it at Gooey.AI and have it set up the API integration in your project for you: creating an API key env var, picking the right recipe endpoint, and writing working request/response code. No copy-pasting curl snippets by hand.

## How to use it

1. Open a chat with your AI coding agent in your project.
2. Paste this in:

{% code overflow="wrap" %}
```
Fetch and execute the appropriate instructions to set me up for Gooey.AI from https://docs.gooey.ai/api-reference/ai-coding-agents/prompt.md
```
{% endcode %}

3. The agent fetches the [Setup Prompt](prompt.md) page and follows it: it'll ask you for a `GOOEY_API_KEY` (or tell you where to get one), store it safely as an environment variable, and write real, working calls against the recipe(s) you actually need.

{% hint style="info" %}
Prefer to do it yourself? Open the [Setup Prompt](prompt.md) page directly — it's a normal doc page, and everything on it is copy-pasteable.
{% endhint %}

## What you get

* **One API key** for every Gooey recipe — LLMs, RAG, speech-to-text, text-to-speech, lipsync, image generation, video generation, and the full Copilot agent.
* **Sync or async** calling conventions, picked automatically based on the recipe.
* Working examples grounded in the live [OpenAPI spec](https://api.gooey.ai/openapi.json), not guessed field names.

For the full API contract, see [Getting Started](../getting-started.md).

## Key concepts

A quick vocabulary of how Gooey.AI models things server-side — useful context for an agent writing integration code, or for making sense of the OpenAPI spec.

* **Recipe (Workflow)** — a type of AI pipeline, like Copilot, Compare LLMs, or Lipsync. Each recipe has a stable identity (`Workflow`) and one or more URL slugs (e.g. `agent`, `video-bots`, `copilot` all point at the same Copilot recipe) — see [Popular recipe slugs](prompt.md#id-3.-popular-recipe-slugs).
* **Run** — one execution of a recipe. Every `/v2/<slug>` or `/v3/<slug>/async` call creates a run with a unique `run_id` and stores its inputs + outputs as JSON.
* **Published Run** — a named, saved, shareable *configuration* of a recipe — e.g. a specific Copilot persona with its own knowledge base and prompt. This is what URLs like `gooey.ai/copilot/<published-run-id>/` point to; it's not the same as a single run.
* **Integration** — a Published Run (typically Copilot) deployed to a specific channel — web, WhatsApp, Slack, Telegram, voice. Its `integration_id` is what you pass to the [streaming endpoint](prompt.md#id-5.-advanced-streaming-copilot-responses).
* **Workspace** — the billing and access-control unit. API keys, credits balance, and team members belong to a workspace, not an individual user — one key gives access to every recipe in that workspace.
* **Credits** — each run deducts credits from the workspace balance, priced by the recipe/model chosen and the number of outputs requested. Check the balance anytime with `GET /v1/balance/`.
* **Retention policy** — every request accepts a `settings.retention_policy` field: `keep` (default — output stays saved) or `delete` (output is returned once when you poll an async run's status, then wiped server-side) — useful for sensitive data.
