---
icon: microchip
description: >-
  Point Gooey Server at Ollama, vLLM, LocalAI, LM Studio or llama.cpp and run
  recipes with no cloud model access at all.
---

# Adding Local AI Models

`setup_local` seeds specs for cloud models (OpenAI, Google, Anthropic), which need the corresponding API keys to actually run. To run Gooey with no cloud model access at all, point it at a local OpenAI-compatible server — **Ollama, vLLM, LocalAI, LM Studio, or llama.cpp** all work.

{% hint style="success" %}
This is pure runtime configuration. No code changes, no forking, no rebuild.
{% endhint %}

## 1. Run the model server

With [Ollama](https://ollama.com), `ollama pull <model>` fetches a model and its server listens on port `11434` by default:

```bash
ollama pull qwen3.5:4b
```

## 2. Register it in the Django admin

Go to **AI Models → AI Model Specs → Add** ([http://localhost:8000/ai\_models/aimodelspec/add/](http://localhost:8000/ai_models/aimodelspec/add/)), set **Category** to `LLM`, and fill in:

| Field                                                      | Value                                                                                     |
| ---------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Name**                                                   | Internal id used in API calls, e.g. `qwen3_5_4b`. Don't change it after use.               |
| **Label**                                                  | UI display name, e.g. `qwen3.5 4b`                                                        |
| **Creator**                                                | Select or add, e.g. `Qwen`                                                                |
| **Model id**                                               | The provider/HuggingFace id, exactly as the server expects it, e.g. `qwen3.5:4b`          |
| **Priority**                                               | Sort order within the creator group                                                       |
| **Provider** (Provider Settings)                           | `OpenAI` — Ollama speaks the OpenAI-compatible API                                        |
| Context Window, Max Output Tokens (Model Settings)         | Per the model; check Chat Model / Thinking Model / Supports Temperature as applicable     |
| **API Key** (API Settings)                                 | `ollama` — a placeholder, it isn't validated                                              |
| **Base URL** (API Settings)                                | `http://localhost:11434/v1`, or wherever you're hosting the model                         |

Click **Save**, and the model shows up in the model pickers.

{% hint style="info" %}
On the [Docker path](installation/quickstart-with-docker.md), `http://localhost:11434/v1` works from inside the containers too: `docker-compose.local.yml` maps `localhost` to the host gateway for every app service.
{% endhint %}

## Beyond LLMs

LLMs are the most common thing to self-host, but they aren't the only one. Embeddings (`intfloat/e5-*`, `thenlper/gte-*`), speech-to-text (Whisper, Seamless M4T, MMS), and text-to-speech (Bark) all run on the self-hosted GPU Celery worker, with cloud providers as optional alternatives behind the same abstraction.

See [Platform Independence](platform-independence.md#4-ai-models-abstraction-layers-with-self-hosted-alternatives-path-2) for the full picture, including where each abstraction lives in the code.
