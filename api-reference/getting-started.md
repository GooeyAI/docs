---
description: You can interact with our APIs through node.js, python or curl
---

# Getting started

Use Gooey.AI's APIs to build fast! Get started by trying these simple setups - **No servers, API keys, or rate limits to manage.**

## Quickstart

{% tabs %}
{% tab title="Orchestration to webview in minutes" %}
Embed your custom AI workflow on your website or app as a webview instantly. Customize the look and feel in seconds.

```javascript
<div id="gooey-embed"></div>
<script>
    function onLoadGooeyEmbed() {
        GooeyEmbed.mount({});
    }
</script>
<script async defer onload="onLoadGooeyEmbed()" src="
https://gooey.ai/chat/gooey-base-copilot-Kbo/lib.js
"></script>
```

Pass custom in-app context

{% code overflow="wrap" %}
```javascript
GooeyEmbed.mount({ payload: { variables: { username: "John Appleseed" }  } });
```
{% endcode %}

{% embed url="https://github.com/GooeyAI/gooey-web-widget" %}
{% endtab %}

{% tab title="Stream AI Responses, Live in Your App" %}
**Real-time results, zero infrastructure**\
Stream AI responses directly to users with tool use, voice, image, and video — all client-side. No servers, API keys, or rate limits to manage.

{% code overflow="wrap" %}
```javascript
// create a stream on Gooey server
let response = await fetch("https://api.gooey.ai/v3/integrations/stream/", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
  },
  body: JSON.stringify({
    // your integration's ID as shown in the Gooey.AI Integrations tab
    "integration_id": "Kbo",
    // the prompt for the bot
    "input_prompt": "Generate a QR code of the taj mahal",
    // full api here: https://api.gooey.ai/docs#tag/Copilot-Integrations/operation/video-bots__stream_create
  }),
});
// get the server-sent events URL
let sseUrl = response.headers.get("Location");
// start listening to the stream
const evtSource = new EventSource(sseUrl);
// handle the stream events
evtSource.onmessage = (event) => {
    // log the message to the console
    console.log(data.type, data);
};
```
{% endcode %}
{% endtab %}

{% tab title="Extend with Functions as a service" %}
**Write Python or JavaScript in our AI IDE — no setup required.**\
Secure, fast code execution in V8 + Docker lets you build custom logic and connect to any service. No YAML, no OpenAPI specs, no DevOps.

Try it out here:

{% embed url="https://gooey.ai/functions/wttr-weather-wi8xj3k0mzbb/" %}

<figure><img src="../.gitbook/assets/FOR DEVELOPERS fold 3 (2).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

## Read the API Docs

{% embed url="https://api.gooey.ai/docs" %}

### Create an API Key

Gooey.AI allows single API key for several workflows. So whether you are including AI images in your app or making a highly customized AI Copilot, you can access our whole suite of workflows through a single API key.&#x20;

CREATE API KEYS HERE:

{% embed url="https://gooey.ai/api/#api-keys" %}

You can click on "Create new secret key"

<figure><img src="../.gitbook/assets/Screenshot 2023-11-02 231541--- (2).png" alt=""><figcaption></figcaption></figure>

A new API KEY will appear

<figure><img src="../.gitbook/assets/Screenshot 2024-01-04 155308.png" alt=""><figcaption></figcaption></figure>

Copy the key and use it for your API Requests.&#x20;

{% hint style="info" %}
Make sure you don't share your API KEY with anyone! 🚫
{% endhint %}

## Authentication

**Remember that your API key is a secret!** Do not share it with others or expose it in any client-side code (browsers, apps). Production requests must be routed through your own backend server where your API key can be securely loaded from an environment variable or key management service.

All API requests should include your API key in an `Authorization` HTTP header as follows:

```
"Authorization": "Bearer " + GOOEY_API_KEY
```

## Making a request

Let's make an example request to the `lipsyncTTS API`

{% tabs %}
{% tab title="node.js" %}
#### Step 1

Install [node-fetch](https://www.npmjs.com/package/node-fetch) & add the `GOOEY_API_KEY` to your environment variables. Never store the api key [in your code](https://12factor.net/config) and don't use direcly in the browser.

```bash
$ npm init
$ npm install node-fetch
$ export GOOEY_API_KEY=sk-xxxx
```

#### Step 2

Use this sample code to call the API. Make sure to include the full code snippet and the error message.

```js
import fetch from 'node-fetch';

const payload = {
  "input_face": "https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/6ce4c720-a799-11ed-9033-02420a0001d8/NEW%20LONG%20VID.mp4",
  "text_prompt": "Add your text prompt for Lipsync TTS here"
};

async function gooeyAPI() {
  const response = await fetch("https://api.gooey.ai/v2/LipsyncTTS/", {
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
{% endtab %}

{% tab title="python" %}
#### Step 1

Install [requests](https://requests.readthedocs.io/en/latest/) & add the `GOOEY_API_KEY` to your environment variables. Never store the api key [in your code](https://12factor.net/config).

```bash
$ python3 -m pip install requests
$ export GOOEY_API_KEY=sk-xxxx
```

#### Step 2

Use this sample code to call the API. If you encounter any issues, write to us at [support@gooey.ai](mailto:support@gooey.ai) and make sure to include the full code snippet and the error message.

<pre class="language-python"><code class="lang-python">import os
import requests

payload = {
    "input_face": "https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/6ce4c720-a799-11ed-9033-02420a0001d8/NEW%20LONG%20VID.mp4",
    "text_prompt": "Add your text prompt for Lipsync TTS here",
<strong>}
</strong>
response = requests.post(
    "https://api.gooey.ai/v2/LipsyncTTS/",
    headers={
        "Authorization": "Bearer " + os.environ["GOOEY_API_KEY"],
    },
    json=payload,
)
assert response.ok, response.content

result = response.json()
print(response.status_code, result)
</code></pre>
{% endtab %}

{% tab title="curl" %}
#### Step 1

#### Install [curl](https://everything.curl.dev/get) & add the `GOOEY_API_KEY` to your environment variables. Never store the api key [in your code](https://12factor.net/config).

```bash
export GOOEY_API_KEY=sk-xxxx
```

#### Step 2

Run the following `curl` command in your terminal. If you encounter any issues, write to us at [support@gooey.ai](mailto:support@gooey.ai) and make sure to include the full curl command and the error message.

```bash
curl https://api.gooey.ai/v2/LipsyncTTS/ \
  -H "Authorization: Bearer $GOOEY_API_KEY" \
  -H 'Content-Type: application/json' \
  -d '{
  "input_face": "https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/6ce4c720-a799-11ed-9033-02420a0001d8/NEW%20LONG%20VID.mp4",
  "text_prompt": "Add your text prompt for Lipsync TTS here"
}'
```
{% endtab %}
{% endtabs %}

#### This is what the example response will look like:

```json
{
  "id": "aghpjaxi",
  "url": "https://gooey.ai/lipsync-maker/?run_id=aghpjaxi&uid=fm165fOmucZlpa5YHupPBdcvDR02",
  "created_at": "2023-05-16T13:48:08.093970+00:00",
  "output": {
    "output_video": "https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/27b18b98-9a96-11ee-a030-02420a0001ca/gooey.ai%20lipsync.mp4"
  }
}
```
