---
description: >-
  Set up a simple workflow to compare ASR models and evaluate the right choice
  for your product
---

# 📊 How to create language evaluation for ASR?

### Why do you need a Bulk and Evaluation Workflow?

When testing ASR models, your main goal is to scope out which model is best suited for your project needs.&#x20;

There are several components to test:&#x20;

* understanding model proficiency in global languages and local accents
* assessing the accuracy of translations
* checking for low Word Error Rate
* latency
* price

### Features of Bulk Runner and Evaluation Workflow

1. Run several models in one click
2. Choose any of the API Response Outputs to populate your test
3. Built-in evaluation tool for quick analysis
4. Use csv or Google Sheets as input
5. Get output in CSV for further data analysis

#### Also see:

<table data-view="cards" data-full-width="true"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td>🏎️ Global Language Understanding for AIs</td><td><a href="https://app.gitbook.com/s/leYcqBx5FRZcVr3wI4f4/global-language-understanding-for-ais">Global Language Understanding for AIs</a></td><td><a href="../.gitbook/assets/gooey.ai - cute robots racing vintage painted magazine advertisement muted colorful illustration.png">gooey.ai - cute robots racing vintage painted magazine advertisement muted colorful illustration.png</a></td></tr><tr><td>🗣️ Check out our Hindi ASR Evaluation</td><td><a href="https://gooey.ai/bulk/compare-hindi-speech-recognition-hkgs8120p11t/">https://gooey.ai/bulk/compare-hindi-speech-recognition-hkgs8120p11t/</a></td><td><a href="../.gitbook/assets/gooey.ai - cute vintage poster style illustration of a small group of indian kids learning hindi (1).png">gooey.ai - cute vintage poster style illustration of a small group of indian kids learning hindi (1).png</a></td></tr></tbody></table>

## Getting Started

### Step 0 - Prepare your data

1. Collect all your audio voice samples into a Google Drive folder (make sure they are in .wav or .mp3 format)
2. In a new Google spreadsheet or CSV file copy the links of all your audio files&#x20;
3. Add the human-created transcription for each sample
4. Add the English translation for each sample

<figure><img src="../.gitbook/assets/Screenshot 2024-05-07 at 12.27.38 AM.png" alt=""><figcaption></figcaption></figure>

### Step 1 - Select the ASR Models

Head to our bulk and eval workflow.&#x20;

[LINK TO HINDI ASR EVALUATION EXAMPLE](https://gooey.ai/bulk/compare-hindi-speech-recognition-hkgs8120p11t/)

In the example, we have already pre-filled the various models that can be tested. You can choose the ones you want to run by selecting it in the dropdown.

<figure><img src="../.gitbook/assets/Screenshot 2024-05-07 at 12.31.01 AM.png" alt=""><figcaption><p>Select the models you want to evaluate your audio samples on</p></figcaption></figure>

### Step 2 - Add your CSV/Google Sheets

Upload your CSV/Google Sheet from [Step 0](how-to-create-language-evaluation-for-asr.md#step-0-prepare-your-data). In this example, we have used a Google Sheet of 10 Audio Samples with transcripts and translations. A preview of your sheet will appear once it is correctly uploaded.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2024-05-07 at 12.34.15 AM.png" alt=""><figcaption></figcaption></figure>

### Step 3 - Select the input column

Select the column in the input from the dropdown box. The outputs will appear as various columns. In this example, it will be the "audios" column

<figure><img src="../.gitbook/assets/Screenshot 2024-05-07 at 12.36.40 AM.png" alt=""><figcaption></figcaption></figure>

### Step 4 - Select the pre-built evaluator

In the "Evaluation Workflows" section select the "Speech Recognition Model Evaluator".

<figure><img src="../.gitbook/assets/Screenshot 2024-05-07 at 12.38.13 AM.png" alt=""><figcaption></figcaption></figure>

### Step 5 - Hit Submit

Once you hit submit, the selected ASR model workflows (see [Step 1](how-to-create-language-evaluation-for-asr.md#step-1-select-the-asr-models)) will run for each audio file in the sheet (see [Step 2](how-to-create-language-evaluation-for-asr.md#step-2-add-your-csv-google-sheets)). An output CSV will be generated on the right-hand side of the page.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2024-05-07 at 12.47.58 AM.png" alt=""><figcaption><p>The outputs will appear in a table format on the right of the page, the output will appear in new columns after your originally populated columns</p></figcaption></figure>

After the runs are complete, the selected Evaluator (see [Step 4](how-to-create-language-evaluation-for-asr.md#step-4-select-the-pre-built-evaluator)), will compare the ASR model outputs to the human-generated translations. It will assess and rate how accurately each model has translated the audio sample.&#x20;

A bar graph with the performance will appear once the entire evaluation is complete.

<figure><img src="../.gitbook/assets/Screenshot 2024-05-07 at 12.50.05 AM.png" alt=""><figcaption><p>After the evaluation is complete, table and a bar graph will show the evalution scores</p></figcaption></figure>



## FAQs

#### Q: How should I prepare the transcription and translation data?

A: Arrange the audio sample link in the first column, for each audio link add transcriptions and translations in the respective row.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2024-05-08 at 11.08.26 PM.png" alt=""><figcaption><p>Screenshot of audio sample links with trasncriptions and english translation</p></figcaption></figure>

#### Q: What is the ideal length of the recording?

A: Any recording less than 40 minutes will work successfully, if you are a copilot creator we would recommend limiting the audio sample to 2-3 minutes.&#x20;

#### Q: What audio format should we use?

A: Gooey's ASR workflow will accept .wav and .mp3 audio formats.

#### Q: How many files can I test?&#x20;

A: Our partners have tested up to 1000 audio files in one run!&#x20;

#### Q: How can we increase the quality of the test?

A: Make sure your transcriptions and translations are as accurate as possible.&#x20;
