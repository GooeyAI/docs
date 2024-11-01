---
description: A simple guide on how to use Automatic Speech Recognition
---

# 🗣️ How to use ASR?

We find speech recognition and translations important when we create AI workflows for frontline workers, traders, and impact organizations.&#x20;

In AI copilot scenarios, we found that users prefer to send queries by voice rather than text. This could mean:&#x20;

* voice notes to Whatsapp and web copilots
* Voice-based IVR in low internet coverage areas

So as part of our [AI Workflow Standards](https://blog.gooey.ai/workflow-standards), we now host over 15 ASR models, that can be chained into the AI Copilot workflows.&#x20;

Here is a simple guide to use the ASR Workflow

### Step 1: Add your audio samples

* Head to the Gooey.AI Speech Recognition and Translation Workflow: [https://gooey.ai/speech/](https://gooey.ai/speech/)
* Click on the "Clear all" Button and upload your audio file via a local folder or a link&#x20;

{% hint style="info" %}
If you are using a link you can use: &#x20;

* a hosted media link&#x20;
* a google drive link of the audio file&#x20;
* youtube video link
{% endhint %}



<div>

<figure><img src="../../.gitbook/assets/Screenshot 2024-10-30 at 1.27.20 PM.png" alt="" width="375"><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/Screenshot 2024-10-30 at 1.28.00 PM.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Step 2: Select the Speech to Text provider&#x20;

* Select the language in "Speech-to-Text Provider" from the dropdown provided.

{% hint style="info" %}
Use the "Filter by Language"  dropdown, if you are unsure which models will work with your source language
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2024-10-30 at 1.35.22 PM.png" alt=""><figcaption></figcaption></figure>

### Step 3: Select your translation model

* Click on the "Translate" checkbox
* Select the translation model of your choice

### Step 4: Click "Run"

* Click on the "Run" button&#x20;

### Frequently Asked Questions <a href="#frequently-asked-questions" id="frequently-asked-questions"></a>

**Q: How do I test the ASR models that can transcribe Swahili?**

A: Use the "Filter by Language" dropdown, if you are unsure which models will work with your source language.

**Q: In the translate section I can see "Google Translate" and "GhanaNLP", which model should I use?**

A: If you are translating an African Language you can test if GhanaNLP is a better choice. GhanaNLP Machine Translation supports: Twi, Ewe, Ga, Fanti, Yoruba, Dagbani, Kikuyu, Fra fra, Luo (Kenya, Tanzania), Meru, Kusaal

**Q: I have tested a few models, but I want to evaluate a larger dataset without using the API, is that possible?**

A: Yes! It is very easy to set up large-scale ASR evaluations in Gooey! Here is the guide for:&#x20;

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>How to create language evaluation for ASR?</strong></td><td><a href="how-to-create-language-evaluation-for-asr.md">how-to-create-language-evaluation-for-asr.md</a></td></tr></tbody></table>

**Q: What is the "Prompt" section when I choose GPT4o-Audio?**

A: GPT4o-Audio is an LLM-based transcription model, the prompt section will allow you to output the transcribed audio in more specific ways. For example, if you input a Hindi audio sample, you can say "Translate the Hindi recording as accurately as possible". This will use the LLM directly to translate the audio. You could also use it in other innovative ways like "Summarize the Hindi recording to English in bullet points" which could give you the salient points of the recording directly. Like the example here:&#x20;

{% embed url="https://gooey.ai/speech/?run_id=1rnoo9r71o3q&uid=fm165fOmucZlpa5YHupPBdcvDR02" %}

