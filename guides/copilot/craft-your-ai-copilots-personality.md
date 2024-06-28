---
description: Optimise and create the best prompt for your AI Copilot
---

# Craft your AI Copilot's personality

### High-level system prompt

This refers to the prompt that defines the character, tone, reasoning process of the bot.&#x20;

Create a small personality/character for your bot stating its name, purpose and who built it.&#x20;

_<mark style="background-color:yellow;">Should it be funny or formal, should it produce long answers or short, should it answer simply or summaries in a more technical way.</mark>_

Here is an example prompt:

> “You are <mark style="background-color:yellow;">Product.CHAT</mark> - an intelligent AI assistant built by Gooey.AI and <mark style="background-color:yellow;">acme.com</mark> to help people understand the basics of <mark style="background-color:yellow;">Javascript coding</mark>. Try to give succinct answers to their questions (at a 6th grade level), taking note that they are beginners and learning how to use Javascript in their example projects.”

{% hint style="info" %}
NOTE: Please replace all the highlighted parts with your own information in the example script&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-22 at 12.35.37 PM.png" alt=""><figcaption></figcaption></figure>

### Create the Task Instructions&#x20;

Once the user sends their query, Copilot will search through the documents and prepare a set of snippets and sources that best answer the query. This requires explicit instructions so that the Copilot can aggregate and summarize the answers as per your requirements.

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-22 at 12.38.07 PM.png" alt=""><figcaption></figcaption></figure>

Here is an example set of Task Instructions:&#x20;

> \[Guidelines]
>
> * Make sure to use only the Search Results to produce a coherent answer
> * If the Search Results provide insufficient information, refuse to answer the question and redirect the user to <mark style="background-color:yellow;">acme.com/tutorials</mark> for more help.
> * If the Search Result's Title or Snippet is unrelated or irrelevant to the question, don't respond and just say you don't know.
> * Never give advice to search the Internet.
> * Politely refuse to answer questions beyond the subject of basics of Javascript and other programming language related subjects.
> * Always use appropriate emojis to emphasize your point.
> * Cite the Search Results using \[${number}] notation in your answer.

{% hint style="info" %}
NOTE: Please replace all the yellow highlight parts with your own in the example task instructions
{% endhint %}

#### Add the Task Instructions

{% embed url="https://youtu.be/b8YMudcCKss" %}
Click on the "Settings" tab to add the Task Instructions
{% endembed %}

### Hit Submit!&#x20;

At this point, your Copilot is ready for testing. However, you might need to do some tweaks to get it production-ready!&#x20;
