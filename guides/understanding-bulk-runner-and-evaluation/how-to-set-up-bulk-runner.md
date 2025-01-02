# 💪 How to set up Bulk Runner?

In this example scenario, we are setting up a simple bulk run to check regression for an AI Copilot in production.

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Check out the example run here: BULK RUNNER (Regression Only)</strong></td><td><a href="https://gooey.ai/bulk/farmerchat-bulk-evaluator-regression-only-ggzy9gld1eae/">https://gooey.ai/bulk/farmerchat-bulk-evaluator-regression-only-ggzy9gld1eae/</a></td></tr><tr><td><strong>Check out the example run here: BULK RUNNER (Bulk and Evaluation)</strong></td><td><a href="https://gooey.ai/bulk/farmerchat-bulk-evaluator-gpt-4o-mixtral-claude-vs-gemini-pro-15-b0o8aos3rj8y/">https://gooey.ai/bulk/farmerchat-bulk-evaluator-gpt-4o-mixtral-claude-vs-gemini-pro-15-b0o8aos3rj8y/</a></td></tr></tbody></table>

{% include "../../.gitbook/includes/bulk-run-credit-warning.md" %}

### Step 1: Select Gooey Workflows <a href="#jmvc9vjmbif9" id="jmvc9vjmbif9"></a>

Choose the “SAVED” run from Gooey.AI Workflows that you would like to use.

![](../../.gitbook/assets/2.png)

### Step 2: Input Data Spreadsheet <a href="#s6plmddmwaiq" id="s6plmddmwaiq"></a>

Prepare your test question set:

1. Create a list of the most frequently asked questions for your AI Copilot (we recommend between 25 for optimum observability and regression you can do more if you prefer)
2. Make sure the Excel sheet/Google Sheets table has a “header” section
3. Add all your questions in the column below it

<figure><img src="../../.gitbook/assets/3.png" alt="" width="369"><figcaption></figcaption></figure>

1. Paste the link of your Google sheet or upload your data

&#x20;

<figure><img src="../../.gitbook/assets/4.png" alt="" width="563"><figcaption></figcaption></figure>

### Step 3: Select your input columns <a href="#yayrw51txj9z" id="yayrw51txj9z"></a>

In the current scenario, we want to use the Gooey Copilot to answer all the questions in the google sheet. So essentially they are the “input” for the Bulk Workflow.

Select the “questions” column in the “Input Prompt” section.

![](../../.gitbook/assets/5.png)

### Step 4: Hit Submit <a href="#pqej8inj371s" id="pqej8inj371s"></a>

As this is a “Bulk only” scenario, you can “delete” the Copilot Evaluator option in the section. After that hit the “Submit” button.

&#x20;

<figure><img src="../../.gitbook/assets/6.png" alt="" width="563"><figcaption></figcaption></figure>

### Output <a href="#id-6n9vkbjh3n11" id="id-6n9vkbjh3n11"></a>

The workflow will create a new CSV, with an added few columns based on the run, including, “Output Text”, “Run URL”, and “Run Time”.

**Your output will be on the right side of the page.**

<figure><img src="../../.gitbook/assets/7.png" alt="" width="563"><figcaption></figcaption></figure>

#### Additional Note <a href="#kfu0hmigziyi" id="kfu0hmigziyi"></a>

If you want more details in the Output section, use the checkboxes in the “Show All Columns” section on the right. This is useful if you want to keep track of Price, Error Messages, and other details.

![](../../.gitbook/assets/8.png)

