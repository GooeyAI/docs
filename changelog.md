---
icon: clock-rotate-left
---

# Changelog

All notable changes to this project will be documented in this file. It keeps track of changes to the GooeyAI repository - [gooey-server](https://github.com/gooeyAI/gooey-server)

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).&#x20;

## Unreleased

* Support for using Seamless M4T v2 for translation and TTS will be made available in the UI soon!

## 20-Aug-2024

#### Added 

* **[LLM](https://gooey.ai/compare-large-language-models)**: Updated [Sarvam](https://www.sarvam.ai/), GPT-4o Mini, [SEA-LION-v2](https://aisingapore.org/aiproducts/sea-lion/). Head over to our Compare LLM Generator to see it in action, [SEA-LION v2](https://gooey.ai/compare-large-language-models/compare-llms-sea-lion-vs-sota-h6anugije1jf/) available here!
* **[Functions](https://gooey.ai/functions)**: Update on the functions editor with in-built linter. 
* **[AI Standards](https://gooey.ai/standards)**: Gooey.AI proposes AI Standards. Checkout our proposal to the Library of Congress and Rockfeller Foundation [here](https://gooey.ai/standards). We propose that shared AI workflows can catalyze innovation everywhere.
* **[Impact](https://gooey.ai/impact)**: Understand how you can use GenAI for your Impact Organization.

## 14-Aug-2024

#### Added

* **Speech Recognition and Translation**: We have upgraded Seamless M4T to v2. This provides improved ASR for nearly 100 languages. Try it here: [https://gooey.ai/speech/seamless-m4t-v2-hindi-english-g8883e8675gk/](https://gooey.ai/speech/seamless-m4t-v2-hindi-english-g8883e8675gk/)
*   **Copilot:** Enabled "Auto-play responses" in **Copilot** Web Widget Integrations. You can control whether audio/video responses should be auto-played or not. This feature is enabled by default.\
    \


    <figure><img src=".gitbook/assets/Auto-play (1).png" alt=""><figcaption></figcaption></figure>

## 8-Aug-2024

#### Added

*   **Lipsync**: We have deployed some improvements around the SadTalker lipsync model&#x20;

    * more understandable error messages,&#x20;
    * support for a wider range of image/video resolutions,&#x20;
    * the ability to not crash on long videos, &#x20;
    * better support for video inputs overall.&#x20;

    Here is an example of the improved performance on video input:&#x20;

_OLD OUTPUT_

{% embed url="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/eef688c8-1dfb-11ef-af8a-02420a000128/gooey.ai%20lipsync.mp4" %}

_NEW OUTPUT_

{% embed url="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/1db03ed8-4ecc-11ef-b5a4-02420a000192/gooey.ai%20lipsync.mp4" %}

#### Fixed

* **Lipsync**: bug fixes for short input audio and reference inputs &#x20;

## 24-Jul-2024

#### Fixed

* Fixed the regression with our eleven labs custom voices support. You should now be able to use your custom 11labs voices using your API key on [https://gooey.ai/compare-text-to-speech-engines](https://gooey.ai/compare-text-to-speech-engines) , [https://gooey.ai/copilot/](https://gooey.ai/copilot/) and [https://gooey.ai/lipsync-maker/](https://gooey.ai/lipsync-maker/)

