---
description: A super simple guide to using our most popular workflow!
---

# How to create AI Animations?

AI Animation Generator is an amazing tool that can create beautiful animations from your AI text prompts. You can use this tool to create AI generated music videos, create short clips to include in your videos and other amazing creative outputs without any film editing software.

{% embed url="https://www.youtube.com/watch?v=IsfPUKEzCgE" %}

### STEP 1 - **Visualize your video**

The Animation Generator uses AI text prompts to create each frame of  the video.

* Visualize each keyframe for the video and describe it in the prompt section\
  &#x20;
* Assign the keyframe

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

### STEP 2 - **Add the Frames and Frame Count**

* You can add more prompts and keyframes as per your video\
  &#x20;
* Add the total number of frames for your video

<figure><img src="https://static.wixstatic.com/media/15a5ef_1c1d90cb678d47be989639ff21cf5710~mv2.png/v1/crop/x_0,y_10,w_485,h_208/fill/w_438,h_188,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Screenshot%202023-06-19%20132555.png" alt=""><figcaption></figcaption></figure>

### STEP 3 - **Hit Submit**

* Just hit "Submit" \
  &#x20;
* Each run can take about 3-6 mins depending on the total number of frames and the frame rate

<figure><img src="https://static.wixstatic.com/media/15a5ef_40d68c70569d4d449dcff9ac9b348dbf~mv2.png/v1/crop/x_355,y_0,w_310,h_193/fill/w_402,h_250,al_c,lg_1,q_85,enc_auto/Screenshot%202023-06-19%20132643.png" alt=""><figcaption></figcaption></figure>

### **Camera Settings**

The camera settings allow the animation to move around as if it was "shot" with a camera using zoom, pan and rotate techniques.

### Setting 1

**Zoom**&#x20;

* Zoom settings can be assigned to the keyframes
* The format for the setting is "frame number:(zoom speed)"&#x20;
* For each keyframe setting you need to separate it by a comma&#x20;
* If you want to zoom-in use positive numbers e.g. "1.004"
* If you want to zoom-in use positive numbers e.g. "-1.004"
* "1" will give you static/no zoom
* Note: Don't use "0.04" or similar

<figure><img src="https://static.wixstatic.com/media/15a5ef_0808dc49c582452fa38f252feb9a942a~mv2.png/v1/crop/x_31,y_0,w_756,h_426/fill/w_441,h_249,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Screenshot%202023-06-19%20132741.png" alt=""><figcaption></figcaption></figure>

### Example

If you wanted to zoom in from 0 - 49 frames and zoom out from 50 - 100 frames&#x20;

```
"0:(1.004),50:(-1.004)"
```

### Setting 2

**PAN**

* Pan settings can be assigned to the keyframes
* The format for the setting is "frame number:(pan direction and speed)"&#x20;
* For each keyframe setting you need to separate it by a comma&#x20;
* If you want to pan left use positive numbers e.g. "2"
* If you want to pan right use positive numbers e.g. "-2"
* Note: Don't use "0.04" or similar

### Example

If you wanted to horizontal pan from 0 - 49 frames and no pan from 50 - 100 frames&#x20;

```
"0:(3),50:(1)"
```

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

### Setting 3

**ROTATE**

* Rotate settings can be assigned to the keyframes
* The format for the setting is "frame number:(rotate direction and speed)"&#x20;
* For each keyframe setting you need to separate it by a comma&#x20;
* If you want to rotate anti-clockwise use positive numbers e.g. "2"
* If you want to rotate clockwise use positive numbers e.g. "-2"
* Note: Don't use "0.04" or similar

<figure><img src="https://static.wixstatic.com/media/15a5ef_a106b16dd386468a9f0d808d6ca99355~mv2.png/v1/fill/w_507,h_362,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Screenshot%202023-06-19%20133154.png" alt=""><figcaption></figcaption></figure>

### Example

If you wanted to rotate left from 0 - 25frames and rotate right from 26 - 50 frames&#x20;

```
"0:(1),25:(-1)"
```

{% embed url="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/5d2106d6-d760-11ed-8c78-02420a00014b/gooey.ai%20animation%20[frame%200%20prompt%20a%20wide%20angle%20...interior%20of%20roller%20coaster%204k%208k%20uhd%201%20people-1].mp4" %}

TRY THE EXAMPLE HERE 👇

{% embed url="https://gooey.ai/animation-generator/?example_id=8nuen2rr" %}

**Additional Resources**

* [Guide to Image Prompting 101](https://docs.google.com/presentation/d/1RaoMP0l7FnBZovDAR42zVmrUND9W5DW6eWet-pi6kiE/edit?usp=sharing)
* [Art styles guide](https://supagruen.github.io/StableDiffusion-CheatSheet/)

VIDEO TUTORIALS

{% embed url="https://www.youtube.com/watch?v=sUvica6UuQU" %}

FOLLOW ALONG WORKSHOP

{% embed url="https://www.youtube.com/watch?v=cg8PpubSkcQ" %}
