---
icon: code
---

# How to use Bulk Run via API

### Step 1

* Run the TTS models you want to test on the UI.&#x20;
* Copy the links of the test runs&#x20;

<figure><img src="../../.gitbook/assets/BULK-RUN-API (3).jpg" alt=""><figcaption></figcaption></figure>

### Step 2

* Open Gooey.AI bulk&#x20;
* Head to the API tab&#x20;
* Click on the “curl” tab

<figure><img src="../../.gitbook/assets/BULK-RUN-API (1).jpg" alt=""><figcaption></figcaption></figure>

EXAMPLE:&#x20;

{% embed url="https://gooey.ai/bulk/compare-swahili-speech-recognition-ehrfs6a0yukt/api/" %}

### Step 3

* Add your CSV/google sheet in the documents section (see a screenshot of the CSV example below)&#x20;
* Add your run URLs in the run\_urls section.
* Point to the correct column for the input in input\_columns

```sh
curl 'https://api.gooey.ai/v2/bulk-runner?example_id=ehrfs6a0yukt' \
  -H "Authorization: bearer $GOOEY_API_KEY" \
  -H 'Content-Type: application/json' \
  -d '{
  "documents": [
    "https://docs.google.com/spreadsheets/d/1EsQ_NKhyNikNNO3xLV9GOc6C5LTflu9dJ5CSpHqNUQs/edit?gid=0#gid=0"
  ],
  "run_urls": [
   "https://gooey.ai/compare-text-to-speech-engines/?run_id=todlwvm01l31&uid=fm165fOmucZlpa5YHupPBdcvDR02",
   "https://gooey.ai/compare-text-to-speech-engines/?run_id=j8v9fqrfl26o&uid=fm165fOmucZlpa5YHupPBdcvDR02",
    ],
  "input_columns": {
    "text_prompt": "Column Name"
  },
  "output_columns": {
    "price": "Price",
    "run_url": "Run URL",
    "run_time": "Run Time",
    "output_text": "Output Text",
    "raw_output_text": "Raw Output Text"
  }
}'
```

<figure><img src="../../.gitbook/assets/Screenshot 2025-01-28 at 2.23.00 PM.png" alt=""><figcaption></figcaption></figure>

### How can I calculate the credits?&#x20;

<figure><img src="../../.gitbook/assets/BULK-RUN-API (2) (1).jpg" alt=""><figcaption></figcaption></figure>

* Please check the credit per run in the sample run you run for your bulk run.&#x20;
* This should be the average cost per run.
* Since you are running Bulk API, you can also check the credits for every run by adding `"price": "Price"` in the `"output_columns"` section
