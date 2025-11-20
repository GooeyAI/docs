---
icon: comments-question-check
---

# How to set up Golden Q\&As

The Golden Q\&A pair helps to test

* Various prompt tweaks to improve the AI Agent's responses
* Compare LLM models
* Compare audio speech, recognition and, text-to-speech models
* Check price and latency
* Monitor regression

With the help of our Bulk and Evaluation Workflows, you can test the AI Agent quickly against a Q\&A set.

{% embed url="https://www.youtube.com/watch?v=qGfhSDoX034" %}

#### Create your Golden Q\&A pair <a href="#id-4y2kttei07z1" id="id-4y2kttei07z1"></a>

Prepare your golden QnA set:

1. Create a list of the most frequently asked questions for your AI Agent (we recommend between 25 for optimum observability and regression you can do more if you prefer)
2. Make sure the Excel sheet/Google Sheets table has a “header” section
3. Add all your questions and golden answers in the column below it

<figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

> **An expert must provide the Golden Answers, these can't be synthetic answers.**

**Common terms**

* **Golden Answer**: Most suitable and accurate answers provided by humans with expertise on the subject
* **Semantic Closeness**: Since LLM will not output the same answer every time, the evaluation will check for how semantically close the output of the LLM is to your “Golden Answer”
* **Score and Rank**: For each generated answer the Evaluation workflow will give a “score” between 0 and 1, and rank the best answer.
* **Reasoning**: Evaluation LLM will share a short "reasoning" of how the score was given
* **Chart**: Based on the aggregate score, the Evaluation workflow will create a comparison chart

### KNOWLEDGE BASE VS GOLDEN Q\&A <a href="#knowledge-base-vs-golden-q-and-a" id="knowledge-base-vs-golden-q-and-a"></a>

| Knowledge Base                                                                                                              | Golden Q\&A                                                                                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The Knowledge base is this entire set of structured and unstructured data that encompasses your agent’s field of expertise. | Golden Q\&A is a sample set of questions and answers. This is sample set includes questions most likely asked by user with an answer most accurately framed by an expert in your team |
| This includes all your web pages, PDFs, CSVs, Docs, and videos.                                                             | This is always a table with 4-5 columns with “Questions” and “Answers” as separate column headers.                                                                                    |
| Exists in your AI Agent Builder                                                                                             | Is meant to be used in the Bulk Evaluation Workflow (we will learn about it in Session 4)                                                                                             |
| Is used directly in your citations for the AI Agent's answers                                                               | Is only meant for testing your AI Agent’s accuracy                                                                                                                                    |
| Meant for answering external users questions                                                                                | Meant for checking regression, quality, time and cost internally                                                                                                                      |
