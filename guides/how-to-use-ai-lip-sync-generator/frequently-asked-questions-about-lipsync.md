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
