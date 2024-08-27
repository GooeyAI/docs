# 🕵️‍♀️ How to set up Evaluations?

In this example scenario, we are comparing and evaluating the quality of the answers of various AI Copilots that have all the same settings and functionalities except for different LLMs.&#x20;

### Step 1: Select Gooey Workflows to evaluate <a href="#mj1hmvoaayxg" id="mj1hmvoaayxg"></a>

Choose the “SAVED” run from Gooey.AI Workflows that you would like to use.

![](../../.gitbook/assets/9.png)

### Step 2: Input Data Spreadsheet <a href="#id-4y2kttei07z1" id="id-4y2kttei07z1"></a>

Prepare your golden QnA set:

1. Create a list of the most frequently asked questions for your AI Copilot (we recommend between 25 for optimum observability and regression you can do more if you prefer)
2. Make sure the Excel sheet/Google Sheets table has a “header” section
3. Add all your questions and golden answer in the column below it



<figure><img src="../../.gitbook/assets/10.png" alt="" width="563"><figcaption></figcaption></figure>

**You must provide the Golden Answers. Golden answers are the most suitable and accurate answers provided by humans with expertise on the subject.**

1. Paste the link of your Google sheet or upload your data&#x20;

<figure><img src="../../.gitbook/assets/11.png" alt="" width="563"><figcaption></figcaption></figure>

### Step 3: Select your input columns <a href="#o6vzivos324o" id="o6vzivos324o"></a>

In the current scenario, we want to use the Gooey Copilot to answer all the questions in the Google sheet. So essentially they are the “input” for the Bulk Workflow.

Select the “questions” column in the “Input Prompt” section.

![](../../.gitbook/assets/12.png)

### Step 4: Hit Submit <a href="#brcrdr2ggss2" id="brcrdr2ggss2"></a>

As this is a “Bulk and Eval” scenario, you can “select” the Copilot Evaluator option in the section. After that hit the “Submit” button.

![](../../.gitbook/assets/13.png)

_Note: We recommend using the “Copilot Evaluator” if you are evaluating Copilot Runs._

### Output <a href="#id-22et24oucovd" id="id-22et24oucovd"></a>

The workflow will create a new CSV, with an added few columns based on the run, including, “Output Text”, “Run URL”, and “Run Time”.

_**With the evaluation option, you will also get output for “Rationale”, “Compare Run Score”, etc. You will also get a Compare Chart which will show the aggregate scores.**_

**Your output will be on the right side of the page.**

<figure><img src="../../.gitbook/assets/Screenshot 2024-08-19 at 4.53.02 PM.png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-08-19 at 11.30.43 PM (1).png" alt="" width="375"><figcaption></figcaption></figure>

### Best Practices <a href="#oucznt5a94xk" id="oucznt5a94xk"></a>

* Keep it simple - try to use an input spreadsheet with limited columns
* Don’t leave any empty data points in the second row - there is a bug and the column does not read
* Make sure to name your “Saved” workflows with relatable titles so that it is easy to set up the run
*   We recommend collecting user messages from your saved copilot's “Analytics” section. Head to Your copilot link> Integrations tab > View Analytics, scroll to the bottom, and **export** the “Messages” tab CSV. \


    <figure><img src="../../.gitbook/assets/16.png" alt=""><figcaption></figcaption></figure>

#### Note: <a href="#id-8grsusqblfge" id="id-8grsusqblfge"></a>

* Bulk runner will only read the first sheet of your Excel or Google Sheet
* In the case of Google Sheets, you can shift your relevant sheet to be the first and then re-enter the link in the Input section. IT WILL NOT REFRESH ON ITS OWN.
