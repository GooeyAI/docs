---
icon: clock-rotate-left
---

# Changelog

All notable changes to this project will be documented in this file. It keeps track of changes to the GooeyAI repository - [gooey-server](https://github.com/gooeyAI/gooey-server) and other changes to the [Documentation](https://docs.gooey.ai/) and the [Gooey.AI](https://gooey.ai/) website.&#x20;

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

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
*   **Copilot:** Enabled "Auto-play responses" in **Copilot** Web Widget Integrations. You can control whether audio/video responses should be auto-played or not. This feature is enabled by default.\


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
