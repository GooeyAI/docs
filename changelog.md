---
icon: clock-rotate-left
---

# Changelog

All notable changes to this project will be documented in this file. It keeps track of changes to the GooeyAI repository - [gooey-server](https://github.com/gooeyAI/gooey-server) and other changes to the [Documentation](https://docs.gooey.ai/) and the [Gooey.AI](https://gooey.ai/) website.&#x20;

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## 30-March-2026

Changed

* Transform message structure for Fireworks chat handling

## 26-March-2026

Added

* Private-chat streaming via `sendMessageDraft`

## 12-March-2026

Added

* Telegram bot Deployment

## 27-February-2026

**Fixed**

* [Guard `query_vespa` against empty/invisible search queries — prevent Vespa 400 "NullItem" errors](https://github.com/GooeyAI/gooey-server/commit/7422aef292c64aef04c7c105181977b55ed859de)
* [Handle `None` keyword\_query in `query_vespa`](https://github.com/GooeyAI/gooey-server/commit/586abcf4200e7f0436360307d32d1fd2d0eb7f9d)

## 25-February-2026

**Added**

* [Batch memory updates from Python/JS functions](https://github.com/GooeyAI/gooey-server/commit/4e33b7a2ba8d51ddf6ac2a70c5a57c42dedc22f1)

## 21-February-2026

**Fixed**

* [Array columns handling in evals](https://github.com/GooeyAI/gooey-server/commit/7135cb66090ea658be2c88d6e96de35bf75a3f56)

## 20-February-2026

**Fixed**

* [Bot-builder videogen inputs schema](https://github.com/GooeyAI/gooey-server/commit/71f2f5a3b0d9af32714d508691b035810fdf4291)

## 18-February-2026

**Fixed**

* [Padding issues; render audio input/output in Copilot; move history filter widget out of base.py](https://github.com/GooeyAI/gooey-server/commit/5f699b2dea7829158ad37c204c2f707594a62e7b)
* [History filter not shown for non-logged-in users](https://github.com/GooeyAI/gooey-server/commit/bf602e7b24d14156b13d621c696f1edc5150ec8d)

## 14-February-2026

**Fixed**

* [Composio "Connect & Grant Access" button redirect](https://github.com/GooeyAI/gooey-server/commit/8ffd1db24ca0bd33a75e399301647568e68ad89e)

## 12-February-2026

**Added**

* [Per-person history on history page](https://github.com/GooeyAI/gooey-server/commit/f70af54dd7b74601d380f1aa1beeff48d797336f)

**Fixed**

* [Preserve whitespace when streaming text](https://github.com/GooeyAI/gooey-server/commit/201b65feead809ebc4a81f1a9b5623e419bb25d0)
* [Video history UI and model name display](https://github.com/GooeyAI/gooey-server/commit/469af185ce8424b787bad739482052dd904d0fcc)
* ["Add variable" button incorrectly creating a new function](https://github.com/GooeyAI/gooey-server/commit/6fd9bafaa68b172a617ef376f2ca8b08b8da227c)

## 04-February-2026

**Fixed**

* [DTMF timeout and disconnects in LiveKit agent loop](https://github.com/GooeyAI/gooey-server/commit/b93fde305fdaa33892a822d7095a5a1cb79e7a23)
* [Support for non-Twilio numbers in LiveKit](https://github.com/GooeyAI/gooey-server/commit/dc27039baa3a6b125ada053fdd170310564cd702)
* [Empty photo URL in branding](https://github.com/GooeyAI/gooey-server/commit/889b182d3832a702aaffcf2df27bb31304f1596a)

## 03-February-2026

**Added**

* [Authentication and credit notification email templates; `error_params` field in SavedRun model](https://github.com/GooeyAI/gooey-server/commit/c01015ddf7da3faf1c0306afa90a13aa8c34d939)

**Fixed**

* [Updated credit costs for image generation models](https://github.com/GooeyAI/gooey-server/commit/8e32439b227c8f518a2220c09c8915e9faf406a9)
* [Copilot web widget branding](https://github.com/GooeyAI/gooey-server/commit/bdb293ed20c7161edfc331ea114233d0fe27df0c)
* [Null variables handling in API; null version retrieval in saved workflow](https://github.com/GooeyAI/gooey-server/commit/a0c3241a5aca56e3b072b2687d87318dd1b6f61f)

## 30-January-2026

**Added**

* [Private Google Drive file access via Composio auth](https://github.com/GooeyAI/gooey-server/commit/cc5986580cf160d8a970a8cc98dca6253138814c)
* [Support for multiple Google Drive accounts via Composio](https://github.com/GooeyAI/gooey-server/commit/1e4c5623e8f6fadfcfd52b72a83dd8b468cb8cd9)

## 26-January-2026

**Added**

* [SSO login support](https://github.com/GooeyAI/gooey-server/commit/44372a07e86af78762b713e64d7d3056f0d886a6)
* [Draft run created every time Gooey Builder updates state](https://github.com/GooeyAI/gooey-server/commit/4d63ca6c6cece5be50775f6e95ed931746b10867)

## 20-January-2026

**Added**

* [Render video URLs from markdown in WhatsApp](https://github.com/GooeyAI/gooey-server/commit/704970a3c07ac57f63719e7d73a05ae07b4151f1)
* [Thinking summary display in Copilot; stream thinking messages](https://github.com/GooeyAI/gooey-server/commit/6ff3114b0761c733edc99a58254b30b1d09b7526)

## 16-January-2026

**Added**

* [Thinking summary in Copilot](https://github.com/GooeyAI/gooey-server/commit/2bb01a9da759d5aaac4443beeaf34a9e29411ea0)

## 15-January-2026

**Added**

* [LiveKit call recording and transcript](https://github.com/GooeyAI/gooey-server/commit/1488b1ec4e0f129669854f9f295f33d173a08deb)

## 14-January-2026

**Added**

* [Support for OpenAI Responses API](https://github.com/GooeyAI/gooey-server/commit/b4c4e7d6d65a21c506acc4452e387b52667a3b53)

## 12-January-2026

**Added**

* [Custom OpenAPI-based model support in LiveKit](https://github.com/GooeyAI/gooey-server/commit/9b5c3d7996f4787777b9fd586690c8c458eff8d3)

## 02-January-2026

**Fixed**

* [Bot builder photo URL picked from branding](https://github.com/GooeyAI/gooey-server/commit/5fae37c043c4d2bcdf2dc1a6830bb8e99d145b7e)

***

## 19-December-2025

**Fixed**

* [Formatting issue in Gooey Builder](https://github.com/GooeyAI/gooey-server/commit/4a1af2b4b7487a135b25855c6ea85aaf32d3f010)

## 18-December-2025

**Fixed**

* [Progress bar z-index order](https://github.com/GooeyAI/gooey-server/commit/83d48acaf4094defef561d97450afa8fd2d4665a)

## 28-November-2025

Changed

* [Videogen schema: add support for non-string enums](https://github.com/GooeyAI/gooey-server/commit/6282d675d551c6393be0b0eb7c90fd1e4777214b)

## 26-November-2025

Changed

* [Use audio input capability for Gemini LLMs](https://github.com/GooeyAI/gooey-server/commit/7a610f536b25771f1d42c6987db59c26546bfe46)

Fixed

* [Only render updated\_at/generated timestamp once](https://github.com/GooeyAI/gooey-server/commit/a683bba6e945c2831bcb4a2881a03fb142c13c5e)

## 25-November-2025

Changed

* [Move MMS TTS & Omnilingual models](https://github.com/GooeyAI/gooey-server/commit/b6936ff51eb0ddfcd5b8437d179e624a552f9b77)

## 21-November-2025

Added

* [Meta Omnilingual ASR model](https://github.com/GooeyAI/gooey-server/commit/ebc19e8b827600d4fb1cb0a2c62b29c8dcbd12b9)

## 19-November-2025

Added

* [Support for GPT-5.1](https://github.com/GooeyAI/gooey-server/commit/79aa874ae1d32308756b8c90bac9298149d401ad)
* [Support for Gemini 3 Pro preview](https://github.com/GooeyAI/gooey-server/commit/135c6bc6447b993ec1b959ca9d56ae2ef8919a22)

## 18-November-2025

Fixed

* [Make modal import lazy](https://github.com/GooeyAI/gooey-server/commit/e4c9a472253833a22105c5e50b64edfb9039bc1a)

## 29-September-2025

_Fixed_

* [cleaner filter for removing image-url content chunks](https://github.com/GooeyAI/gooey-server/commit/e4339f693f6ae233370a62f408019953225e0246)

## 25-September-2025

_Fixed_

* [remove rank from order\_by when search is empty](https://github.com/GooeyAI/gooey-server/commit/9b808f0debd425ab1fc037fc8579002a37282c12)

## 24-September-2025

_Added_

* [render pricing notes and example preview on video gen](https://github.com/GooeyAI/gooey-server/commit/45ef6e6bcc1a1d0965c2ad8b0bb6f158ee54f69d)

## 18-September-2025

_Fixed_

* [image input creates invalid API request for apertus model](https://github.com/GooeyAI/gooey-server/commit/d672282380c5b2995ddddb113e10cfe6a41b3024)

## 16-September-2025

_Added_

* [implement LiveKit voice agent with Twilio integration](https://github.com/GooeyAI/gooey-server/commit/43dcc31430920628941e669d84d733c82071746e)

## 15-September-2025

_Added_

* [add support for Nano Banana](https://github.com/GooeyAI/gooey-server/commit/e10c19e3526c8ae3569c7634155718b57ded1612)
* [add explore link in header](https://github.com/GooeyAI/gooey-server/commit/bd158e66da29c177029a7b16bb73e02054055534)

## 11-September-2025

_Added_

* [add support for SwissAI Apertus LLM](https://github.com/GooeyAI/gooey-server/commit/607f57c15526a4d5ca329ec167af7216dab5dd78)

## 25-August-2025

**Added**

* [version stats](https://github.com/GooeyAI/gooey-server/commit/ae6ad719aa8580ff3654502612e677957011f365)

## 22-August-2025

**Added**

* [implement reasoning\_effort for openai, claude and gemini](https://github.com/GooeyAI/gooey-server/commit/db8e9fc259e35cfd8d922635f4db0d043a786c97)

## 21-August-2025

**Added**

* [add mbaza asr model](https://github.com/GooeyAI/gooey-server/commit/b3f664741127a40a642e796b683733a742b6019a)

## 20-August-2025

**Added**

* [combined analysis plot with correct data & timezone selector](https://github.com/GooeyAI/gooey-server/commit/83517ff46f6522f1472165e2e936625e59e8ef33)

## 18-August-2025

**Added**

* [add gemini 2.5 flash lite](https://github.com/GooeyAI/gooey-server/commit/d0a8b00225c38a5286c8ee5679345b13cea59d37)

## 14-August-2025

**Added**

* [bulk runs on copilot](https://github.com/GooeyAI/gooey-server/commit/d89fb3ae4f4610573fd19ede64a6e9f056e2f076)

## 13-August-2025

**Added**

* [Aspect ratio icons and functionality to DeforumSDPage](https://github.com/GooeyAI/gooey-server/commit/0b3d58d38375408825df417b9d6b77052c3c55d6)
* [Support for reasoning\_effort for OpenAI and Gemini thinking models](https://github.com/GooeyAI/gooey-server/commit/df6c25efc905e6f9321b79baba00556dd815ff5b)

## 12-August-2025

**Added**

* [Show "Open Workspace" on public team page for non-admins](https://github.com/GooeyAI/gooey-server/commit/e66d9a26188547bf459851cdb77c4ae27be07d4c)

## 09-August-2025

**Added**

* [Added GPT-5 Models](https://github.com/GooeyAI/gooey-server/commit/55d181c6cb996b99e6a21e31b5bcab841cfe709d)

## 22-July-2025

**Added**

* [Added Flux.1 Kontext \[pro\]](https://github.com/GooeyAI/gooey-server/pull/736)

## 08-May-2025

**Added**

* [Added o3, o4-mini, 4.1, 4.1-mini, and 4.1-nano](https://github.com/GooeyAI/gooey-server/pull/646)
* [Added gpt 2.5 flash preview model](https://github.com/GooeyAI/gooey-server/pull/655)
* ["Help guide" button in workflow header](https://github.com/GooeyAI/gooey-server/pull/657)

**Changed**

* [Clearer wording on share dialog](https://github.com/GooeyAI/gooey-server/pull/652)
* [Changed placement for visibility on the workflow list](https://github.com/GooeyAI/gooey-server/pull/652)
* [Changed workflow list to show workspaces name in front of user pill](https://github.com/GooeyAI/gooey-server/pull/656)

**Fixed**

* [Bugfix for Gemini 2.5 pro preview: lower bound for max tokens to accommodate thinking tokens](https://github.com/GooeyAI/gooey-server/pull/653)

## 18-Nov-2024

**Fixed**

_UX:_

* Removed the signout button from the profiles page (now we have the profile dropdown) - ([commit](https://github.com/GooeyAI/gooey-server/commit/2404a1e97eb54e8669024896f661033c2c4ce7f8))
* Use an icon with more click-space for more options in the menu
* Fixed bug where the share button disappears from a saved run - ([commit](https://github.com/GooeyAI/gooey-server/commit/e0a9119b0ccab0ef68d63c11e53af4d1cc4f2786))
* Support change notes for saved runs&#x20;
* Better button placement in version history&#x20;

**Added**

_Workspaces \[beta]:_&#x20;

* Breadcrumbs in workspace>author style ([commit](https://github.com/GooeyAI/gooey-server/commit/0d93d32720033f9f8a07f417904e803824d1feaa))&#x20;
* Better invitation email text ([commit](https://github.com/GooeyAI/gooey-server/commit/2c94b7c321aaabddf3ebb4a131dc2853eccefb32))&#x20;
* Better text labels for account pages ([commit](https://github.com/GooeyAI/gooey-server/commit/40c02993e8289880643293da8b16964109083aa1))
* Show workspace selector in "Save" dialog ([commit](https://github.com/GooeyAI/gooey-server/commit/557184bd6e1fce0d7e3583e6fd9bfe8bdce75e55))
* Added URL fragments to the reference links for improved redirection to specific sections on cited webpages [#502](https://github.com/GooeyAI/gooey-server/pull/502)

## 11-Oct-2024

**Fixed**

* Render correct run cost estimate when something on the page changes [#475](https://github.com/GooeyAI/gooey-server/pull/475)

**Added**

* Ability to select LLM on /eval [#472](https://github.com/GooeyAI/gooey-server/pull/472)
* UX improvements to "save as new" / "save" for anon & logged in users ([#453](https://github.com/GooeyAI/gooey-server/pull/453), [#481](https://github.com/GooeyAI/gooey-server/pull/481))
* New "share" dialog for published runs [#453](https://github.com/GooeyAI/gooey-server/pull/453)

## 17-Sep-2024

#### Added

* Beta release of Python SDK - [https://github.com/gooeyai/python-sdk](https://github.com/gooeyai/python-sdk) and [https://pypi.org/project/gooeyai/](https://pypi.org/project/gooeyai/)
* Improve OpenAPI spec to use the standard security scheme definition for Bearer

#### Fixed:

* Bug fix for SERP search location when set to st

## 11-Sep-2024

#### Added

* Updated web widget chat with a [sidebar to contain conversation history](https://github.com/GooeyAI/gooey-web-widget/commit/0dccc94c36a276fd49c91aa247fdfb2e073b0daa)
* [All error codes are available in the documentation](https://docs.gooey.ai/api-reference/error-codes)

## 03-Sep-2024

#### Added

* [Updated GPT-4o to `gpt-4o-2024-08-06` with support for **16,384 output tokens**](https://github.com/GooeyAI/gooey-server/commit/8274b3d4513ce4fcc63a125f386fd582d24b029c)
* Added support for [Gemini 1.5 Flash](https://deepmind.google/technologies/gemini/flash/) and [ChatGPT-4o models](https://platform.openai.com/docs/models/gpt-4o)
* Support for JSON mode on Gemini 1.5 Pro, Gemini 1.5 Flash, and Claude
  * Try here:  [LLM JSON Output](https://gooey.ai/compare-large-language-models/lesson-plan-json-mode-bfmfw2xqksd7/)

## 28-Aug-2024

#### Added

* [Allow auto-recharge for users without a paid subscription](https://github.com/GooeyAI/gooey-server/commit/bb334bc7314577c6fb13d0c0d6a12e15343ac39a)
* Allow saving payment method after a top-up for easier payments in the future
* Updated meta descriptions for: https://gooey.ai/llm and https://gooey.ai/copilot&#x20;
* [Rate limits page](https://docs.gooey.ai/api-reference/rate-limits)

#### Fixed&#x20;

* [Regression on top-up payments with PayPal](https://github.com/GooeyAI/gooey-server/commit/200d559250b43cebbd02f8c19e9438b64306923f)

## 20-Aug-2024

#### Added

* [**LLM**](https://gooey.ai/compare-large-language-models): Updated [Sarvam](https://www.sarvam.ai/), GPT-4o Mini, [SEA-LION-v2](https://aisingapore.org/aiproducts/sea-lion/). Head over to our Compare LLM Generator to see it in action, [SEA-LION v2](https://gooey.ai/compare-large-language-models/compare-llms-sea-lion-vs-sota-h6anugije1jf/) and [Sarvam](https://gooey.ai/compare-large-language-models/compare-smol-models-ffutnq5io8g4/) available here!
* [**Functions**](https://gooey.ai/functions): Revamped functions editor with an in-built linter.
* [**AI Standards**](https://gooey.ai/standards): Our proposal to the Library of Congress and Rockefeller Foundation on how shared AI workflows can catalyze innovation everywhere.
* [**Impact**](https://gooey.ai/impact): Understand how you can use GenAI for your Impact Organization.

## 14-Aug-2024

#### Added

* **Speech Recognition and Translation**: We have upgraded Seamless M4T to v2. This provides improved ASR for nearly 100 languages. Try it here: [https://gooey.ai/speech/seamless-m4t-v2-hindi-english-g8883e8675gk/](https://gooey.ai/speech/seamless-m4t-v2-hindi-english-g8883e8675gk/)
*   **Copilot:** Enabled "Auto-play responses" in **Copilot** Web Widget Integrations. You can control whether audio/video responses should be auto-played or not. This feature is enabled by default.<br>

    <figure><img src=".gitbook/assets/Auto-play (1).png" alt=""><figcaption></figcaption></figure>

## 8-Aug-2024

#### Added

*   **Lipsync**: We have deployed some improvements around the SadTalker lipsync model

    * more understandable error messages,
    * support for a wider range of image/video resolutions,
    * the ability to not crash on long videos,
    * better support for video inputs overall.

    Here is an example of the improved performance on video input:

_OLD OUTPUT_

{% embed url="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/eef688c8-1dfb-11ef-af8a-02420a000128/gooey.ai%20lipsync.mp4" %}

_NEW OUTPUT_

{% embed url="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/1db03ed8-4ecc-11ef-b5a4-02420a000192/gooey.ai%20lipsync.mp4" %}

#### Fixed

* **Lipsync**: bug fixes for short input audio and reference inputs

## 24-Jul-2024

#### Fixed

* Fixed the regression with our eleven labs custom voices support. You should now be able to use your custom 11labs voices using your API key on [https://gooey.ai/compare-text-to-speech-engines](https://gooey.ai/compare-text-to-speech-engines) , [https://gooey.ai/copilot/](https://gooey.ai/copilot/) and [https://gooey.ai/lipsync-maker/](https://gooey.ai/lipsync-maker/)
