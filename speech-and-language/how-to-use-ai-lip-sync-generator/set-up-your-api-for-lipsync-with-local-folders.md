---
description: >-
  Here is a quickstart guide to setting up your API with local folders. Go
  through the tabs for node.js or python!
---

# Set up your API for Lipsync with Local Folders

### Step 1 - Start a new Node.js project with `npm init`

{% tabs %}
{% tab title="node.js" %}
#### Install node-fetch and add your API key

1. Start a new node.js project
2. Install node-fetch and add your API key

```bash
$ npm init -y
$ npm install node-fetch
$ export GOOEY_API_KEY=sk-xxxx 
```
{% endtab %}

{% tab title="python" %}
#### Install requests & add the GOOEY\_API\_KEY to your environment variables.

```bash
$ python3 -m pip install requests
$ export GOOEY_API_KEY=sk-xxxx
```
{% endtab %}
{% endtabs %}

### Step 2 - Setup up your local folders with input files

To use [GOOEY.AI lipsync tool](https://gooey.ai/Lipsync/) you need **two types of input files for the project**:

1. **Input face**
   * This is refered to as `input_face` in the API
   * Use the following formats - mp4 / mov / png / jpg
   * Ensure the face has clear human features with eyes, nose, lips. Non-human faces will not work
2. **Input audio**
   * This is referred to as `input_audio`
   * Use the following formats only - wav / mp3

For ease of use make sure the folders are all located in the same project. In this example, we have added the `input_face` and `input_audio` in the folder `lipsync-bulk`.

### Step 3 - Create your `app` file

{% tabs %}
{% tab title="node.js" %}
#### Create your `index.js` file

Copy the example code below to test your API call.

```javascript
// save this in index.js

import fetch, { FormData, fileFrom } from 'node-fetch';

const payload = {};

async function gooeyAPI() {
  const formData = new FormData()
  formData.set('json', JSON.stringify(payload))
  // add the path to your input face
  formData.append('input_face', await fileFrom('lipsync-bulk/image.png'))
  // add the path to your input audio
  formData.append('input_audio', await fileFrom('lipsync-bulk/audio_2024-03-26_11-00-36.ogg.wav'))

  const response = await fetch("https://api.gooey.ai/v2/Lipsync/form/", {
    method: "POST",
    headers: {
      "Authorization": "Bearer " + process.env["GOOEY_API_KEY"],
    },
    body: formData,
  });

  if (!response.ok) {
    throw new Error(response.status);
  }

  const result = await response.json();
  console.log(response.status, result);
}

gooeyAPI();
```

#### Replace with your file paths

In the code above, replace the file paths as per the location of your local file location.

```javascript
//this is the code snippet that needs to be replaced 

formData.append('input_face', await fileFrom('lipsync-bulk/image.png'))
formData.append('input_audio', await fileFrom('lipsync-bulk/audio_2024-03-26_11-00-36.ogg.wav'))
```
{% endtab %}

{% tab title="python" %}
#### Create your `main.py` file

Copy the example code below to test your API call.

```python
// save this in main.py

import os
import requests
import json

files = [
    ("input_face", open("lipsync-bulk/image.png", "rb")),
    ("input_audio", open("lipsync-bulk/audio_2024-03-26_11-00-36.ogg.wav", "rb")),
]
payload = {}

response = requests.post(
    "https://api.gooey.ai/v2/Lipsync/form/?run_id=fecsii61rs6e&uid=fm165fOmucZlpa5YHupPBdcvDR02",
    headers={
        "Authorization": "Bearer " + os.environ["GOOEY_API_KEY"],
    },
    files=files,
    data={"json": json.dumps(payload)},
)
assert response.ok, response.content

result = response.json()
print(response.status_code, result)
```

#### Replace with your file paths

In the code above, replace the file paths as per the location of your local file location.

```python
//this is the code snippet that needs to be replaced 

files = [
    ("input_face", open("lipsync-bulk/image.png", "rb")),
    ("input_audio", open("lipsync-bulk/audio_2024-03-26_11-00-36.ogg.wav", "rb")),
]
```
{% endtab %}
{% endtabs %}

### Step 4 - Run your app

Test if your app is working correctly

{% tabs %}
{% tab title="node.js" %}
Run:

```bash
$ node index.js 
```

If you did everything correctly should get a response like this:

{% code overflow="wrap" %}
```bash
200 {
  id: 'm0rghxk55xfx',
  url: 'https://gooey.ai/Lipsync/?run_id=m0rghxk55xfx&uid=fm165fOmucZlpa5YHupPBdcvDR02',
  created_at: '2024-03-26T06:01:57.449762',
  output: {
    output_video: 'https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/5abbbb76-eb36-11ee-8c54-02420a00014c/gooey.ai%20lipsync.mp4'
  }
}
```
{% endcode %}
{% endtab %}

{% tab title="python" %}
Run:

```bash
$ python main.py
```

If you did everything correctly should get a response like this:

{% code overflow="wrap" %}
```bash
200 {'id': 'enqn22dnppiy', 'url': 'https://gooey.ai/Lipsync/?run_id=enqn22dnppiy&uid=fm165fOmucZlpa5YHupPBdcvDR02', 'created_at': '2024-03-26T06:39:44.768886', 'output': {'output_video': 'https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/a227237e-eb3b-11ee-a294-02420a000146/gooey.ai%20lipsync.mp4'}}
```
{% endcode %}
{% endtab %}
{% endtabs %}
