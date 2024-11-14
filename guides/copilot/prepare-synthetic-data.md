---
description: Learn how to add AI synthesized data to improve your AI Copilot results
---

# Prepare Synthetic Data

### Why do you need synthetic data for AI Copilot?

Often AI Copilots must respond succinctly and answer in FAQ style. &#x20;

When using direct transcriptions from video tutorials and recordings for your [Knowledge Base Documents](curate-your-knowledge-base-documents.md), you will need some synthetic data to ensure the user's query is recognized and answered correctly. Video or audio tutorials, can often be very long sentences and have a casual tone of conversation. This can hinder the AI Copilot's search and summary ability. For this, we recommend using our Synthetic Document Extractor workflow.&#x20;

### Features of Synthetic Document Extractor&#x20;

1. Extract information from videos for various purposes
2. Collect lists of YouTube videos or PDFs for data crunching.
3. Update Google Sheets as workflow progresses.

#### LINK TO WORKFLOW: [https://gooey.ai/doc-extract](https://gooey.ai/doc-extract)

### Step 1: Create a New Google Sheet

Create a new, empty Google sheet to store your extracted data. Set the access permissions to "Anyone with link can edit."

### Step 2: Enter Raw Data links

What will work:

* Hosted video and audio links
* Youtube links
* PDFs (OCR and Tabulated Data will work)

{% hint style="info" %}
PRO TIP: If you copy the link to the Google Folder with your docs/pdf. You should immediately see all the files in the folder
{% endhint %}

### Step 3: Add instructions&#x20;

Open the settings tabs and add the relevant instructions for the synthetic data conversion. Example below:

> You are a Javascript tutor. Read the video training transcripts and create a properly outputted data with the sections with the following headings: Provide a short and succinct title, with an additional delimiter at the title's end - Description: provide an short summary of the video as a description Facts: succinct and accurately list all the facts from the transcription that will be useful to the students; don't self reference the video. FAQs: think about the questions that students would ask for this Javascript course based on the transcripts. Remember the notes below:
>
> * make a comprehensive set of questions and answers based on the transcript
> * avoid repetitions
> * avoid self referencing the course
> * don't make up questions and answers beyond contents of the transcript

### Step 4: Select a Model

Choose a Language model for the synthetic data extraction among the available options.

### Step 5: Select ASR Model

Choose the relevant ASR Model that will work best for your speech recognition.&#x20;

### Step 6: Hit SUBMIT

Hit "Submit." The tool will prepare the sheet and update it in real-time. It will then auto-populate all the needed information along with a transcription.

### Harnessing Additional Functions

Synthetic Data Extractor Workflow allows you to upload all videos from your YouTube playlist through one playlist link, which gives an entire transcription output. Likewise, you can manually choose a list of videos for specific transcription tasks.&#x20;

{% hint style="info" %}
Note: Adding new data on the same sheet may overwrite the saved information.
{% endhint %}

{% hint style="info" %}
The tool works best for content that is less than 30-40 minutes due to word limit restrictions on Google Sheets.
{% endhint %}

#### Transcription Bonus: Extract Data from PDFs

This tool also supports the extraction of data from PDFs. Simply paste the link of the accessible PDF in the input and hit "Submit." Like videos, it will extract important data from your document while also updating a Google sheet in real-time.&#x20;



Tutorial available here:

{% embed url="https://www.youtube.com/watch?v=p7ZLb-loR_4" %}
