---
description: Customise your Copilot settings to fit your business use case
---

# Advanced Settings

### Settings

We offer a wide range of settings to customize the AI Copilot.&#x20;

### Document Search Settings

When a user asks a question, the first task is to search all the relevant documentation. There are several instructions that can be added at this stage that ensure search results are accurate and serve the Language Model with the right snippets to summarize. A basic set of "Guidelines" are already populated, you can change out your website link and other information as needed. &#x20;

<div align="center">

<figure><img src="../../.gitbook/assets/Screenshot 2023-10-27 at 5.07.45 PM.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

> \[Guidelines]
>
> * Please ask the user once for their location, gender, crop(s) they grow to improve your answer to their questions.
> * Make sure to use only the Search Results to produce a coherent answer
> * If the Search Results provide insufficient information, refuse to answer the question and redirect the user to https://www.digitalgreen.org/videos for more help.
> * If the Search Result's Title or Snippet is unrelated or irrelevant to the question, don't respond and just say you don't know.
> * Never give advice to search the Internet.
> * Politely refuse to answer questions beyond the subject of farming in India.
> * Always use appropriate emojis to emphasize your point.
> * Cite the Search Results using \[${number}] notation in your answer.

### Citation style

Based on where the copilot is hosted and your need, several citation styles have been provided.&#x20;

<figure><img src="../../.gitbook/assets/image (15).png" alt="" width="375"><figcaption></figcaption></figure>

### Document Embeddings  Weightage - Dense to Sparse

Usually, we default the weightage setting to 0.5. If you have a copilot that needs to answer with details and with several steps, you can increase the weightage to towards 1. If your copilot must extract hyper-specific keywords or data from tables, we recommend tending the weightage to 0.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-22 at 12.41.58 PM.png" alt=""><figcaption></figcaption></figure>

### Summarization and Keyword Extraction

#### Summarization

For many AI copilots, it will be important to have a context of the conversation history so it can give contextual details and maintain consistency in the answers. In the summarization instructions, we have added a default instruction. You can change this as per your requirement.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2023-10-27 at 5.08.05 PM (1).png" alt="" width="375"><figcaption></figcaption></figure>

#### Keyword Extraction

If your AI Copilot has a lot of tabular data, specific model numbers, addresses, phone numbers, and entity names. You add a prompt instruction for keyword extraction as well. See example below:

> \{{ final\_search\_query \}} Extract rare terms like part numbers from the message. If you can't find rare terms, return an empty string. Don't use quotes in your response, instead write the output as a list of tab separated keywords.

{% hint style="info" %}
If your AI Copilot does not require conversation history context or keyword searches, you can keep the sections empty. This will decrease the overall prompt size and improve latency.
{% endhint %}

### Knowledge Base Speech Recognition&#x20;

Choose the relevant language for your Knowledge Base Documents (your prepared documents)

<figure><img src="../../.gitbook/assets/Screenshot 2023-10-27 at 5.08.17 PM (1).png" alt="" width="375"><figcaption></figcaption></figure>

### Language Model Settings

Gooey hosted a range of Language Models that are open source and paid. Please chose the one that suits your needs the most.

<figure><img src="../../.gitbook/assets/Screenshot 2023-10-27 at 5.09.29 PM (1).png" alt="" width="375"><figcaption></figcaption></figure>

### User Language Settings

If the copilot end users will send messages in languages other than English, please add that detail here. This will translate the user's message to English internally to provide better search and summarization and then translate the bot responses back from English to the user language.

<figure><img src="../../.gitbook/assets/Screenshot 2023-10-27 at 5.09.34 PM (1).png" alt="" width="375"><figcaption></figcaption></figure>

### Fine Tuned Language Understanding with Custom Glossaries

Once a user language is selected, two glossaries can be provided. 1) The input glossary which the LLM will use to translate/understand the incoming user messages and 2) The output glossary which the LLM will use to translate its responses back to the user language. These can be csv, tsv, excell, or google sheet files either uploaded manually or via url (the latter will automatically update when translating if the url content has changed):

&#x20;

<figure><img src="../../.gitbook/assets/image (19).png" alt="" width="375"><figcaption></figcaption></figure>

The glossary files follow the format specified by the Google Translate API's Equivalent Term Sets ([https://cloud.google.com/translate/docs/advanced/glossary#equivalent\_term\_sets\_csv](https://cloud.google.com/translate/docs/advanced/glossary#equivalent\_term\_sets\_csv)). First row should be [ISO-639](https://wikipedia.org/wiki/ISO\_639) or [BCP-47](https://tools.ietf.org/html/bcp47) language codes. Two extra columns are allowed: “pos” to specify part of speech and “description” (these columns are currently ignored by the Google Translate API but may be used in the future):\


<figure><img src="https://lh7-us.googleusercontent.com/YQC5keBX8eKEOsZXmKrvKN-lI8y8ZUh4KCBHGC2N8rqxcfhrlnc0WzmWrNX3y_kgKn2AcRKYdfWgPrAgvBDJPdKhb9TqrxMm4oNGfDcgsDi1YRmUXxxj9cSNW26C2I3w36A_or_g-b-ZcqLc2aldGEo" alt=""><figcaption></figcaption></figure>

Each subsequent row is then one glossary term in multiple languages. Read more [here](https://cloud.google.com/translate/docs/advanced/glossary#translate\_v3\_translate\_text\_with\_glossary-drest).

**What does this mean**: When translation is done, terms will first be looked up in the relevant glossary in the column of the input language, and if they exist, they will be translated to the corresponding value in the same row of the output language column. If they don't exist, the default (Google Translate) translation will be used.

**Important**: Since the input glossary looks up terms in the \<User Language> column, this column should uniquely map to English terms (i.e. the same user language term should not appear on different rows with different English terms since then it is undefined which English term to use to translate that user language term). Similarly, the output glossary should have its English terms map uniquely to the \<User Language> terms. In the case of multiple non-English languages, these are the potential \<User Language>s so they should satisfy the unique constraints on each glossary for predictable results.

**Note**: The reason we allow multiple languages (and not just English and the User Language specified in the web ui settings) is because the copilot integrations allow switching the user language on the fly for different users, different whatsapp numbers, slack channels, etc. so the overall Copilot example/run needs to allow multiple languages.

**Why/when to use**: Glossaries are good for company and product names (e.g. Gooey.AI) and domain specific terminology that Google Translate does not know. They can also be used to clarify use case specific translation preferences, e.g. enforce formal translations such as using "mother" over "mom" even when the translation source is less formal or clarifying that ambiguous words like "chili" should always refer to the plant (not the powder, dish, etc.) for the specific use case (say a chatbot for farmers). Glossaries can effectively solve these discrepancies and ambiguities across language differences.

**Why/when not to use**: If the desired grammar of the translations, the overall tone, or sentence structure is significantly different for the domain specific purpose vs general use, then a custom trained model might be easier than trying to patch Google Translate defaults one term at a time. Glossaries cannot capture more complex translation logic at the phrase or paragraph level. They are made for individual terms.

### Voice / TTS Settings

Finally, if you feel the user will need voice or video output for the messages, please enable Audio and Video Output. More about TTS Settings can be found in this section.

<figure><img src="../../.gitbook/assets/Screenshot 2023-10-27 at 5.09.50 PM (1).png" alt="" width="375"><figcaption></figcaption></figure>

