---
description: Some answers to common issues when implementing Copilot in production
---
# Frequently Asked Questions about AI Copilot 

### Q: The copilot seems to answer the question accurately but the answers are incomplete. What can I do?

A: To avoid this, you need to increase the Output Tokens from the “settings” section of your copilot. 

> NOTE: If your copilot use case requires a lot of memory/history of the previous chats to continue the conversation this can create huge context windows and you might get a quickly scaled up usage and higher billing. 

### Q: We are running a voice-based bot, the TTS model reads out the formatting syntax like asterisks, hyphens, etc. This is very disturbing to the user. What can we do? 

A: You can add a simple prompt instruction: “Don't include markdown” or if you want to be a lot more specific you can write a detailed prompt like this: 

```
“Remember, you are a voice agent, so do not use markdown, HTML, latex or any other markup language, instead, output plain text without any formatting characters like asterisk, hyphen, bracket, hash, underscore etc. Keep your responses concise and clear under 100 words.”
```

### Q: The copilot is running on Whatsapp for text and Twilio for phone audio, I want to make sure that some prompts are specified only to Twilio, I don’t want to make two bots. What can i do?

A: For example, if you want to make sure that Twilio does not use markdown but you want formatting for your Whatsapp or Web bots. You can add “if statement” to the prompt through our Jinja templating language like this: 

```
{% if platform == "TWILIO" %}
Remember, you are a voice agent, so do not use markdown, HTML, latex or any other markup language, instead, output plain text without any formatting characters like asterisk, hyphen, bracket, hash, underscore etc. Keep your responses concise and clear under 100 words.
{% endif %}
```

> NOTE: This can be added in your basic prompt instructions there are no “special” settings for this. 

### Q: I have a whatsapp/slack copilot, but the text output is showing up as markup language. How can I fix this? 

A: By incorporating _Jinja_ templating in the Prompt, you can adjust the prompt as needed. In the example below we are using Whatsapp and Slack clients running alongside your web-client you can try this example in your AI Copilot: 

```
You are an AI Bot that runs the front-desk of a Dentist's clinic.

{% if platform == [ "WHATSAPP", "SLACK" ] %}
Remember, you are a {{ platform }} agent, so do not use HTML, latex or any other markup language, instead use only the following formatting styles: 
italic: single underscore
bold: single asterix. Do not use 2 asterix as per markdown, instead use {{ platform }} guidelines and use 1 asterix only
strikethrough: single tilde
code: single backtick
code block: 3 backticks
quoted text: place an angle bracket and space before the text
headings: just use bold style with 1 asterix.
{% endif %}
```

Here the Jinja templating language uses an `if statement` to provide the prompt with a condition to output the text in a particular way based on the platform the bot is integrated to. 