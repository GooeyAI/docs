---
description: Rate limits for Gooey.AI API
---

# Rate Limits

Rate limits are restrictions that our API imposes on the number of times a user or client can access our services within a specified period of time.

### Why do we have rate limits? <a href="#kchtzx3a4k15" id="kchtzx3a4k15"></a>

Rate limits are a common practice for APIs, and they're put in place for a few different reasons:

* **They help protect against abuse or misuse of the API.**
* **Rate limits help ensure that everyone has fair access to the API.**
* **Rate limits can help Gooey.AI manage the aggregate load on its infrastructure.**

| **Tier**     | **Rate Limits**                    |
| ------------ | ---------------------------------- |
| **Free**     | 2 concurrent runs, 6 requests/min  |
| **Creator**  | 4 concurrent runs, 10 requests/min |
| **Business** | 4 concurrent runs, 10 requests/min |

### How do these rate limits work? <a href="#jtp4v5fk0x48" id="jtp4v5fk0x48"></a>

At Gooey.AI, we measure rate limits in two ways:

* Number of runs that can run simultaneously
* RPM (requests per minute).

However, as we host several models from across the GenAI ecosystem, there might rate limits on Tokens Per Day, Images Per Day, etc. Please refer to the[ OpenAI guide for Token Limits](https://platform.openai.com/docs/guides/rate-limits/usage-tiers) and the[ Eleven Labs guide for the TTS rate limits](https://help.elevenlabs.io/hc/en-us/articles/14312733311761-How-many-requests-can-I-make-and-can-I-increase-it).

Note:

* Rate limits are defined at the user and org level
* Rate limits may vary by the model being used at the model provider level.

**If you require a higher number of concurrent requests, please reach out to our Sales team via (sales \[at] gooey \[dot] ai).**
