---
description: >-
  A Step-by-Step Guide to Creating Your Own Multi-modal, Multi-Linugal AI
  Copilot
---

# Building a Multi-Modal Copilot

{% embed url="https://youtu.be/ZKjNGxKTMd0" %}

### Introduction

In this tutorial, we're going to create a Multi Modal and Multi Lingual AI Copilot that can be extremely helpful for religious studies or as a study guide for any textbook. We'll be focusing on building a bot, specifically a BibleBot, that can interact with users on platforms like WhatsApp or Facebook. This bot will be capable of analyzing pictures of Bible pages and engaging in meaningful conversations about the content.

{% hint style="info" %}
We support incoming and outgoing languages from Whisper v3 + v2, Google Chirp, Meta Seamless and Azure
{% endhint %}

### TRY THE BIBLE BOT HERE:

{% embed url="https://gooey.ai/bots/?example_id=iiyv5ch7" %}

### Step 1: Setting Up the Bot's Identity

#### Accessing the Workflow

\- Navigate to the Gooey homepage.

\- Click on "Explore" to view the available workflows.

#### Customizing the Bot

\- Select the co-pilot workflow.

\- Rename it to "BibleBot."

\- Edit the initial prompt to introduce BibleBot to users. For example:

> <mark style="background-color:yellow;">Hello! Welcome to BibleBot. I'm an AI designed to help you better understand the Bible. You can send me a text or a voice note with any Bible-related question, and I'll give you a great answer. I'm constantly trying to improve, so please give your feedback by tapping the up-down buttons.</mark>

### Step 2: Uploading the Bible PDF

\- Download a PDF version of the Bible, such as the Holy King James version.

\- Go to the "Downloads" folder and upload the PDF to the bot. The file size might be around 10 megabytes.

### Step 3: Enabling Image Recognition

\- To allow users to take pictures of the Bible, set up the bot with photo intelligence capabilities.

\- Avoid using GPT Vision for OCR as it may not be very effective.

\- Opt for GPT-4 Turbo for faster processing.

\- In the “Photo Intelligence” dropdown configure the bot to extract text from images and provide responses&#x20;

<figure><img src="../../.gitbook/assets/Photo From Sean Blagsvedt.png" alt="" width="375"><figcaption><p>Here we have uploaded a passage from the Bible, with a specific question. The bot uses OCR and GPT4-Vision and provides an answer to the question. </p></figcaption></figure>

### Step 4: Configuring Voice Responses

\- Enable the bot to read back answers to the user.

\- Use a service like Google Voice for text-to-speech functionality.&#x20;

### Step 5: Submitting and Processing

\- After setting up the bot, hit "Submit" to start the embedding process.

\- The bot will process the uploaded Bible PDF, which may take some time depending on the size of the document.

\- The processed text is stored in a cache for quick access in future interactions.

### Step 6: Crafting the Bot's Guidelines

#### Initial Prompt

\- Define what the bot is and how users should interact with it.

\- Provide clear instructions for when a user greets the bot.

#### Response Guidelines

\- Establish rules for how the bot should search for answers within the Bible text.

\- Decide how the bot should handle questions when sufficient information is not available in the Bible:

to refuse either  - Choose to either refuse to answer or attempt to provide a relevant response.

\- Set limitations on the topics the bot can discuss, focusing on the Bible and Christianity.

\- Optionally, include the use of appropriate emojis for a more engaging experience.

### Conclusion

Once you've completed these steps, your BibleBot will be ready for a demo. This bot serves as a powerful tool for engaging with religious texts and can be adapted for other educational purposes. Remember to test the bot thoroughly and make adjustments based on user feedback to ensure the best possible experience.

\
