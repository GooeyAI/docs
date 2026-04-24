# API Tips for AI Image Generator

## BASICS FOR ALL MODELS

### PROMPT (REQUIRED)

A text description of the desired image(s). The maximum length is 4000 characters for dall-e-3.

```
“text_prompt”: "string", 
```

### SELECTED MODELS <a href="#dall-e-3-api" id="dall-e-3-api"></a>

Since our AI Image Generator tool allows you to compare images, you can chose more than 1 model in a single API call.&#x20;

Here is an example of how to use multiple models.&#x20;

{% code overflow="wrap" %}
```
"selected_models": ["dream_shaper","protogen_5_3"]
```
{% endcode %}

**This is the entire list of models we currently host and their API names:**

| Model Name                              | API Name            |
| --------------------------------------- | ------------------- |
| DreamShaper (Lykon)                     | "dream\_shaper"     |
| Dreamlike Photoreal 2.0 (dreamlike.art) | "dreamlike\_2"      |
| Stable Diffusion V2.1 (stability AI)    | "sd\_2"             |
| Stable Diffusion V1.5 (stability AI)    | "sd\_1\_5"          |
| DALL·E 2 (OpenAI)                       | "dall\_e"           |
| DALL·E 3 (OpenAI)                       | "dall\_e\_3"        |
| Open Journey v2 beta (PromptHero) 🐢    | "openjourney\_2"    |
| Open Journey (PromptHero) 🐢            | "openjourney"       |
| Analog Diffusion (wavymulder) 🐢        | "analog\_diffusion" |
| Protogen v5.3 (darkstorm2150) 🐢        | "protogen\_5\_3"    |

<mark style="background-color:orange;">🐢 The turtle emoji indicates that these models run slower</mark>

## Dall-E 3 API Parameters <a href="#dall-e-3-api" id="dall-e-3-api"></a>

Here are the required parameters to get Dall-E 3 images via the Gooey.AI API

### STYLE (REQUIRED)

style (‘natural’ or ‘vivid’): The style of the generated images. Must be one of vivid or natural. Vivid causes the model to lean towards generating hyper-real and dramatic images. Natural causes the model to produce more natural, less hyper-real-looking images. Defaults to ‘vivid’.

```
"dall_e_3_style": "natural",
or
"dall_e_3_style": "vivid",
```

### QUALITY (REQUIRED)

quality (‘standard’ or ‘hd’): The quality of the image that will be generated. ‘hd’ creates images with finer details and greater consistency across the image. Defaults to ‘standard’.

```
"dall_e_3_quality": "hd",
or
"dall_e_3_quality": "standard",
```

### EXAMPLES

Here is an example prompt that gave different results with different Style and Quality settings for Dall-E 3

{% code overflow="wrap" fullWidth="false" %}
```
Innovate a movie poster for a film of a genre of your choosing, such as sci-fi, and give it a title, like ‘Space World’.
```
{% endcode %}

**STANDARD AND VIVID**\
Try it here:&#x20;

{% embed url="https://gooey.ai/compare-ai-image-generators/?run_id=hi3aooqd&uid=fm165fOmucZlpa5YHupPBdcvDR02" fullWidth="false" %}

<div align="center">

<figure><img src="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/4d720f10-ba85-11ee-bfee-02420a000132/gooey.ai%20-%20Innovate%20a%20movie%20poster%20for%20a%20film%20of...%20as%20sci-fi%20and%20give%20it%20a%20title%20like%20Space%20World..png" alt="" width="375"><figcaption></figcaption></figure>

</div>

**STANDARD AND NATURAL**

Try it here:&#x20;

{% embed url="https://gooey.ai/compare-ai-image-generators/?run_id=c023z26i&uid=fm165fOmucZlpa5YHupPBdcvDR02" %}

<figure><img src="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/7fb9bdc8-ba86-11ee-af7d-02420a00012e/gooey.ai%20-%20Innovate%20a%20movie%20poster%20for%20a%20film%20of...%20as%20sci-fi%20and%20give%20it%20a%20title%20like%20Space%20World..png" alt="" width="375"><figcaption></figcaption></figure>

**HD and VIVID**

Try it here:&#x20;

{% embed url="https://gooey.ai/compare-ai-image-generators/?run_id=yf8heqzk&uid=fm165fOmucZlpa5YHupPBdcvDR02" %}

<figure><img src="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/a91d1368-ba9a-11ee-9180-02420a000197/gooey.ai%20-%20Innovate%20a%20movie%20poster%20for%20a%20film%20of...%20as%20sci-fi%20and%20give%20it%20a%20title%20like%20Space%20World..png" alt="" width="375"><figcaption></figcaption></figure>

**HD and NATURAL**

{% embed url="https://gooey.ai/compare-ai-image-generators/?run_id=4w3yalvi&uid=fm165fOmucZlpa5YHupPBdcvDR02" %}

<figure><img src="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/235622d2-ba9b-11ee-806a-02420a0001a4/gooey.ai%20-%20Innovate%20a%20movie%20poster%20for%20a%20film%20of...%20as%20sci-fi%20and%20give%20it%20a%20title%20like%20Space%20World..png" alt="" width="375"><figcaption></figcaption></figure>

#### KNOW MORE

If you want to know more about DALL-E 3 prompting and settings - have a look at this cookbook!&#x20;

[https://cookbook.openai.com/articles/what\_is\_new\_with\_dalle\_3](https://cookbook.openai.com/articles/what\_is\_new\_with\_dalle\_3)
