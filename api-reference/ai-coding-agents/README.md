---
description: Connect an AI coding agent (Claude Code, Cursor, Copilot, etc.) to the Gooey.AI API and have it wire up the integration for you.
---

# 🧑‍💻 AI Coding Agents

## What is this?

If you build with an AI coding agent — [Claude Code](https://claude.com/claude-code), Cursor, GitHub Copilot, Windsurf, or similar — you can point it at Gooey.AI and have it set up the API integration in your project for you: creating an API key env var, picking the right recipe endpoint, and writing working request/response code. No copy-pasting curl snippets by hand.

This works the same way as Cloudflare's ["agent setup"](https://developers.cloudflare.com/agent-setup/) flow: there's a plain-text [Setup Prompt](prompt.md) hosted at a stable URL. You give your agent one line, it fetches that URL and follows the instructions itself.

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
