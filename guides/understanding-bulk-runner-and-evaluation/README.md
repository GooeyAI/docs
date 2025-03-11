# ⚖️ Understanding Bulk Runner and Evaluation

## Why do you need bulk runner and evaluations? <a href="#id-4zynvpxsa8kj" id="id-4zynvpxsa8kj"></a>

When building your Gooey.AI workflows, you will have to tweak the settings often to ensure the responses show parity and are grounded and verifiable.

**There are several components to test:**

* testing prompts
* ensuring the synthetic data retrieval works
* checking the suitability of the language model and its advanced settings
* Latency of generated answers
* evaluation of the final AI Copilot to produce the Golden Answers
* evaluation of the price per run
* regression tests

How can you do this at scale?

**This is where Gooey.AI’s Bulk and Evaluation features shine!**

## Features of Bulk Runner and Evaluation <a href="#eheq9i411cm3" id="eheq9i411cm3"></a>

* Run several models in one click
* Run several iterations of your workflows at scale
* Choose any of the API Response Outputs to populate your test
* Get output in CSV for further data analysis
* Built-in evaluation tool for quick analysis
* Use CSV or Google Sheets as input

## Quickstart

Here are the **quickstart guides** for Bulk Runner and Evaluation:

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td>How to set up Bulk Runner?</td><td><a href="how-to-set-up-bulk-runner.md">how-to-set-up-bulk-runner.md</a></td><td><a href="../../.gitbook/assets/Bulk Runner.png_400x400.png">Bulk Runner.png_400x400.png</a></td></tr><tr><td>How to set up Evaluation?</td><td><a href="how-to-set-up-evaluations.md">how-to-set-up-evaluations.md</a></td><td><a href="../../.gitbook/assets/W.I.9.png_400x400.png">W.I.9.png_400x400.png</a></td></tr></tbody></table>

## How Does Bulk Runner Work? <a href="#r7so22ymyyn2" id="r7so22ymyyn2"></a>

### Bulk Run Overview <a href="#id-2v61ngoeupi4" id="id-2v61ngoeupi4"></a>

This diagram details the process of generating AI-driven answers to a set of test questions using a Language Model (LLM) with Retrieval-Augmented Generation (RAG) capabilities.&#x20;

![](<../../.gitbook/assets/Understanding Bulk run and Evaluations.jpg>)



**1. Test Question Set**

The process begins with a curated set of questions. Examples of such questions include:

\- "What is the lipsync tool's API?"

\- "What is the step-by-step method to make a good animation?"

**2. Bulk Run**

Your “Saved” AI Copilot run processes the entire question set. Each question is individually processed to generate the corresponding answers.

**3. Generated Output Texts**

The generated answers are compiled into an output table. Each question is paired with its respective AI-generated response. For example, the answer to "What is the lipsync tool's API?" provides detailed information regarding the API's functionality and integration methods.

## How Does Evaluation Work? <a href="#id-5anc46np4cur" id="id-5anc46np4cur"></a>

### Comparison and Evaluation Overview <a href="#id-6yuy9sd29g76" id="id-6yuy9sd29g76"></a>

This section details the process for comparing and evaluating generated answers against a set of golden answers to assess their semantic and technical accuracy.

![](<../../.gitbook/assets/Understanding Bulk run and Evaluations (1).jpg>)

1. **Input: Questions and Golden Answers**
   1.  **Test Question Set**: A curated set of questions to be answered, such as:

       \- "What is the lipsync tool's API?"\
       \- "What is the step-by-step method to make a good animation?"
   2. **Golden Answers Set**: Expert-generated answers serve as the benchmark for evaluation.
2. **Bulk Runs**\
   The test question set undergoes multiple bulk runs with differently configured Copilot Runs. Eg, you can have various runs where you have tweaked the prompts, or you wish to test out which LLM would answer your questions the best\
   \
   The test questions are processed to produce a corresponding set of Generated Answers.
3.  **Compare and Evaluate**\
    The generated answer sets from each bulk run are compared against the golden answers to evaluate their accuracy.

    \
    **Scoring**: Each generated answer set is scored based on its semantic and technical accuracy relative to the golden answers.

In this example:

* **Generated Answer Set 1**: Scores 0.8, indicating it is 80% close in accuracy.
* **Generated Answer Set 2**: Scores 1.0, indicating perfect alignment with the golden answers.
* **Generated Answer Set 3**: Scores 0.6, indicating 60% accuracy.

The iterative bulk runs and systematic comparison provide a framework for improving AI-driven answer generation.

## When do you use Bulk vs Bulk+Eval vs Eval? <a href="#z8de5cdl1xxq" id="z8de5cdl1xxq"></a>

* [**Bulk workflow only**](https://gooey.ai/bulk/farmerchat-bulk-evaluator-regression-only-ggzy9gld1eae/) - If you want to test your Copilot’s functionality for regression tests, monitoring and observability, and bugs.
* [**Bulk and Eval** ](https://gooey.ai/bulk/farmerchat-bulk-evaluator-gpt-4o-mixtral-claude-vs-gemini-pro-15-b0o8aos3rj8y/)- If you are testing improvements on your prompts, or updating your documents, want to consider A/B testing.
* [**Eval** **workflow only**](https://gooey.ai/eval/copilot-evaluator-artpuhzwvily/)- If you already have test data and want to use “LLM as Judge” to evaluate it

### Common terms <a href="#id-3yvzoyislzdo" id="id-3yvzoyislzdo"></a>

* **Golden Answer**: Most suitable and accurate answers provided by humans with expertise on the subject
* **Semantic Closeness**: Since LLM will not output the same answer every time, the evaluation will check for how semantically close the output of the LLM is to your “Golden Answer”
* **Score and Rank**: For each generated answer the Evaluation workflow will give a “score” between 0 and 1, and rank the best answer.
* **Reasoning**: Evaluation LLM will share a short "reasoning" of how the score was given
* **Chart**: Based on the aggregate score, the Evaluation workflow will create a compare chart that
