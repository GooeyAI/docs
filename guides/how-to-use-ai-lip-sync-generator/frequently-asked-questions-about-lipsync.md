---
description: Some answers to common issues when implementing Lipsync in production
---

# Frequently Asked Questions about Lipsync

### Q: Can we process a full video while only applying lip sync to specific segments? We're trying to personalize welcome messages, changing one word {name} to the user's name. For example: "Hey {name}, thanks for signing up for our service." We only need the user's name to be lip-synced.

A: We don’t offer this yet, but you can make API calls with only the {name} and stitch it with a fixed video that says "..thanks for signing up for our service.".&#x20;

Here is a Gooogle Colab sample to set this up with our API:&#x20;

{% embed url="https://colab.research.google.com/drive/1qnqVW7H2fiuV3RVMNPtVeaVkBhb7c898?usp=sharing" %}

### Q: I'm getting a message on lipsync projects about "truncated to 250 frames". What does this mean?

<figure><img src="../../.gitbook/assets/Screenshot 2025-01-04 at 12.52.36 AM (1).png" alt=""><figcaption></figcaption></figure>

A: 250 frames cut-off applies to the input video you have added to the Lipsync workflow - if your video is 24 fps the output will be \~10s, at 60 fps it'll be \~4s and so on. If you use an image for the lipsync input instead of a video, the default if 25fps so thats \~10s again. There is no cut-off once [upgrade](https://gooey.ai/account/billing/) to a paid subscription!

### Q: How to clear LipSync history

A: If you are using Gooey.AI API we support this via a simple “keep” or “delete” as an API/SDK request parameter:&#x20;

```
"settings": {
"retention_policy": "delete"
}
```

If you are using the Gooey.AI web app, please fill out this form and we will action your request in 5-7 business days. [https://forms.gle/zgMVzQ4iiaAeRcpG8](https://forms.gle/zgMVzQ4iiaAeRcpG8)&#x20;

### Q: What are the rate limits for creating lipsync videos?

A: You can find out more about rate limits on our pricing page based on the plan you are on: https://gooey.ai/pricing

### Q: What limitations are there on the volume of lipsync videos I can create?

A: If you are using Lipsync with your audio inputs, you can control the audio gain before uploading the audio. If you are using Lipsync with our TTS tools, you may have to edit this in post-production.&#x20;

\
\
