---
description: >-
  After you've connected your AI agent to Slack or WhatsApp, you can send custom
  messages to your users to notify them of relevant news, reengage inactive
  users, and more!
---

# Broadcast Messages (via web or API)

## Using the Web-Based Graphical Interface

Navigate to the [integrations tab](https://gooey.ai/copilot/integrations) on the published run that you've connected. Expand "Configure Settings 🛠️" and scroll to the bottom of the settings. For supported deployment types like Slack and WhatsApp, you should see the following input widget:

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>The Broadcast Widget. Allows entering text and uploading audio, video, and miscellaneous file attachments. Hit "Send Broadcast" and subsequently click "confirm" to send a message to all your users!</p></figcaption></figure>

Enter your message and upload audio, video, and other documents as desired. Make sure the file type is supported by the relevant platform. WhatsApp currently supports `audio/aac`, `audio/mp4`, `audio/mpeg`, `audio/amr`, and `audio/ogg`. Slack has the best support for `audio/mp4` or `audio/mpeg`. Once you're ready to send the messages, click "Send Broadcast" and you'll be prompted for confirmation. Upon confirmation, the messages will start sending. Depending on how many users you have, it can take a few minutes for all of them to be notified.

{% hint style="info" %}
Note that WhatsApp restricts free-form message sending to users who have contacted you within the last 24 hours to prevent spam. To sidestep this issue, you can have your message templates [approved by WhatsApp](https://www.facebook.com/business/help/2055875911147364). To do this, you must use a custom WhatsApp business deployment on Gooey and not one where we manage the number for you. If you have questions, don't hesitate to contact us via [support@gooey.ai](mailto:support@gooey.ai).
{% endhint %}

## Programmatic Access via API

The API supports a few extra features including only sending the message to some subset of users or adding custom buttons. To get started, click the [API link ](https://api.gooey.ai/docs#operation/video-bots__broadcast)(either here or from the deployment tab shown above) to view the API documentation for message broadcasting.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>API documentation for broadcasting.</p></figcaption></figure>

### Specifying which Deployment to Broadcast through

You'll use some combination of the `example_id` and `run_id` query parameters to specify which of your connected published runs you want to broadcast through. These are the same parameters you'll see in the URL on Gooey.AI when you are [editing your run](https://gooey.ai/copilot) or on the [integrations tab](https://gooey.ai/copilot/integrations). To find your run, find it in your history and click on the title to activate it. Then inspect the URL, e.g. "[https://gooey.ai/copilot/farmerchat-with-vision/?example\_id=nuwsqmzp](https://gooey.ai/copilot/farmerchat-with-vision/?example_id=nuwsqmzp)" -- in this case, we only have the "example\_id" query parameter so "https://api.gooey.ai/v2/video-bots/broadcast/send/?example\_id=nuwsqmzp" would be our API endpoint URL.

### Example Code

Once you have your API endpoint, you are ready to start making requests. Here's some sample code in Python, NodeJS, and via [CURL](https://everything.curl.dev/get):

```python
# $ python3 -m pip install requests
# $ export GOOEY_API_KEY=sk-xxxx

import os
import requests

payload = {"text": "Hi, we've launched a new feature: you can now upload photos of your crops and ask questions about them!"}

response = requests.post(
    "https://gooey.ai/copilot/farmerchat-with-vision/?example_id=nuwsqmzp",
    headers={
        "Authorization": "Bearer " + os.environ["GOOEY_API_KEY"],
    },
    json=payload,
)
assert response.ok, response.content

result = response.json()
print(response.status_code, result)
```

```javascript
// $ npm install node-fetch
// $ export GOOEY_API_KEY=sk-xxxx

import fetch from 'node-fetch';

const payload = {"text": "Hi, we've launched a new feature: you can now upload photos of your crops and ask questions about them!"};

async function gooeyAPI() {
  const response = await fetch("https://gooey.ai/copilot/farmerchat-with-vision/?example_id=nuwsqmzp", {
    method: "POST",
    headers: {
      "Authorization": "Bearer " + process.env["GOOEY_API_KEY"],
      "Content-Type": "application/json",
    },
    body: JSON.stringify(payload),
  });

  if (!response.ok) {
    throw new Error(response.status);
  }

  const result = await response.json();
  console.log(response.status, result);
}

gooeyAPI();
```

```bash
# export GOOEY_API_KEY=sk-xxxx

curl 'https://gooey.ai/copilot/farmerchat-with-vision/?example_id=nuwsqmzp' \
  -H "Authorization: Bearer $GOOEY_API_KEY" \
  -H 'Content-Type: application/json' \
  -d '{
  "text": "Hi, we have launched a new feature: you can now upload photos of your crops and ask questions about them!"
}'
```

### Filtering Users

To only broadcast messages to certain subsets of users, we provide some filter options. These include&#x20;

* "wa\_phone\_number\_\_in": list\[string],
* "slack\_user\_id\_\_in": list\[string],
* "slack\_user\_name\_\_icontains": string,
* "slack\_channel\_is\_personal": boolean

They can be added to the filter object of the payloads in the above example code. For example, to only broadcast to the WhatsApp accounts with phone numbers "1234" and "+1 (420) 666-6969", you could modify the payload to the following:

```python
payload = {
    "text": "Hi, we've launched a new feature: you can now upload photos of your crops and ask questions about them!",
    "filters": {
        "wa_phone_number__in": ["1234", "+1 (420) 666-6969"]
    }
}
```
