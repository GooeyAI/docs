---
description: How to set up slack
---

# Deploy to Slack

[Contact us](https://www.help.gooey.ai/contact) for help setting up a bot for your enterprise and integrating it into your platform. Mentioned below are the instructions for the Slack Integration.

{% embed url="https://www.loom.com/share/210c5a724f474de58153e02f222d7a3f?sid=80cf5bf5-6d14-4a60-b6c7-a272f535f784" %}

### Terminology

* Integrations - These are options on the [Integration Page](https://gooey.ai/copilot/integrations/) (specific whatsapp numbers, specific Slack Workspace channels) that a Copilot run/example can be connected to.
* Personal Channels - These are private channels that the bot creates for each user in a channel it is connected to so they can converse privately with the bot.
* Single Channel Members - This is a Slack feature that allows you to add members to your Slack workspace with limited permissions to one channel. Slack integration cannot create personal channels for these users as the Slack permissions forbid it.

## Adding the Copilot Bot to a Slack Workspace

Once you have created a Copilot run/example, you can go to the [Integration Tab](https://gooey.ai/copilot/integrations/) (make sure your run/example id is in the url) and add your bot to WhatsApp, Slack, Facebook, any website with Landbot, and more.

{% hint style="info" %}
Slack integration currently does not support channels with single channel members, since personal channels can’t be created for these.
{% endhint %}

1. First you select an example or run (by clicking 'Tweak' or hitting 'Submit' to save your current settings), then go to the integrations page and click "Add Your Slack Workspace".\
   ![](https://lh7-us.googleusercontent.com/70IbZGhZ-wHmSu8MKP6g7FrS7mE0GBeOIpFDISqS6RhKTdqjs2B-AL6aNph_uY4q8XuITVkhLYpfb3Ww3cgGJSyIiBh1h-1un209PrsMoHISKxK9aq4rcaPv2C492qe1aaJkvlSoXhn9vfMFZvz07j4)
2. This will take you to a page where you select the workspace (upper right corner) and which channel to import (bottom centre) as an integration option into Gooey.AI. Both public and private channels work, however your own active user has to be a member of the private channel for the integration to work if the channel is not public. Otherwise, you can’t grant the bot access rights to this channel.\
   ![](https://lh7-us.googleusercontent.com/cS5nlKpe7fD-_zY1Bas6BySMQOJgppRkCnSrk-Q6heyVrfSMUA0dxQ5m1QL87ioWX_PKLYANlg8PjeTqJu5VJl_OW3KgPWhdidFeLIkgSyGXUfnGhlrgqOlx5JxVGjPyY8rQBkDwZn4UJIkSQJJnJ9w)
3. Upon clicking “Allow”, you should see a message confirming it was successful (you will be prompted to login to Gooey.AI first if you are not already logged in).![](https://lh7-us.googleusercontent.com/3YpTMloz3qQ0bzYR0_RsIcNpfn39RHF-Z0TYdWdOZ3KqKh2jsl-jZbedomnpuC86H6B6a3i0dbqutXPsbgAwIqb9kViigwseIoJeLle3oUrsb_QD-qnh09YEXBTJdqrXL_cdAIzbfLLD6IhdS57SzDI)
4. You can then go back to the integration page and after refreshing, the channel integration option should be visible:\
   ![](https://lh7-us.googleusercontent.com/u8imjpHZnh2c5dODnvid_AJQABtW9UoqveaXezY9OQYWC_zrKDCXsIZ69PywyXFbTtUB5P5hiOXTyqZfw2ADSiZX0qUtTU9kBrhOami-IfGWq2y6ek2rk_wCU-gkLuZDDiUxhwg63m2X1YNu4xQiywY)
5. Click "Connect" to connect your run or example (make sure a run or example is selected by verifying their respective ID is in the URL). Subsequently, your selected channel will receive the following confirmation message:

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

6. Send any message (text or audio) in this channel and the bot will respond in the relevant thread. The bot keeps track of a separate message history for each user (on a per-channel basis) to respond in context.\
   ![](<../../.gitbook/assets/image (8).png>)\

7. You can also chat with the bot with a separate (private) conversation history in the personal channel that it created with all members when connected (it'll create new personal channels for newly joining members as well):\
   ![](<../../.gitbook/assets/image (6).png>)
8. You can always remove the bot or change its display configuration by choosing it in the App pane on the left in your Slack workspace (see next section for details):\
   ![](https://lh7-us.googleusercontent.com/-AaPlnWeKYhFXyjmoHfSc0Ojln1t2dUpdLvB7y2YDjj8-IfjyMKLIV1jy0JgzNeWEc_zPXvECdvQWmiM806t4SuIZWc6kzlyKgh_8rba4r7Bxm3P7KhrHlgg5mbfU4rFJkZZXYdIH-gCb7ljS0qdwwA)
9. To change the data your chatbot uses, any of its other functionality parameters, or the name it posts as in each channel, you need to go to the [Gooey.AI website](https://gooey.ai/copilot/) (see next sections for Slack specific details and refer to the other [Copilot Guides](https://gooey.ai/docs/guides/build-your-ai-copilot) for general settings).

### Adding the Bot in Multiple Languages

{% hint style="info" %}
For now the integration specific language can only be configured by us, so [contact us](https://www.help.gooey.ai/contact) and we'll get language support set up for your integration.&#x20;
{% endhint %}

1. Create a channel for each language in your Slack Workspace
2. Create a run for each language by setting the user language to the corresponding language code using the settings dropdown on the [run tab](http://localhost:3000/copilot/):\
   ![](https://lh7-us.googleusercontent.com/WJsqtHBBcvO-N7QKWgVofH0DpBLbs1G59yZi_BME3svvI7Pw8OU0jorWzfeyRhkbjJqXX_hg2WpCFcfyLcmX_OH4-foOL1vQ1eNNSAAW4An_mUwSNSKHlIFufVvY3d3IMBGs0MQHpuDqgEm2ajMBR-Q)
3. Hit submit after selecting each language to save a run with this language setting.
4. Follow the steps in the [previous section](deploy-to-slack.md#adding-the-copilot-bot-to-a-slack-workspace) for adding the run to your Workspace on the channel you created for it.
5. The bot should send a confirmation message in the respective channels when added which will let you know that the language was correctly configured.

## Configuring the Slack App/Bot

### Change the App Name

This is the name that appears in the Slack Workspace’s “Apps” list and in the initial message of the Bot Integration.

1\. Open the app details by right clicking the app in the Apps list on the left bar:

![](https://lh7-us.googleusercontent.com/zFX-jdGwzNfth4GEaW01AiyUAjXAMhA9PgTnsCFhcIOmzP4BB6ZzF5wL5w4QJK4-9fm2fBHK7ZClktjjRcIiJw2jylb4ulgRmXoj0BlzcD5yz7zsJHMhIPvTC-kux590bjLG_8hgwcLWX0g5KYBcMt4)

2\. Click "Configuration":

![](https://lh7-us.googleusercontent.com/CdtnYMTHURPFPLkkWAjEpzYZl9gk0G261tmQSWEUHZjhFaypCPovUMaKhnNSKKmDr78S3IytnKjYK7uEP3XgERLEcWqBctW1wnzciWHNHHREmBFu5cc9Krecdi90iznlXW9ySPu5_HnqJqCPyuSC_1s)

3\. Scroll down to "Bot User" and click "Edit":

![](https://lh7-us.googleusercontent.com/pT-taqI1vHyKBj7sNTvsVCIumW6uLl2E-o9n_1hhelNwbrbqrCGBx6jZIy5NTjyH2uqFFvf5ijV4gYNogYe9g4ohrciAHgTE00M72x60ts5AgdUbCgQUUGNHw_1LcBtvaCLhQL3MxJmRk_MUdZtvOXI)

4\. You can now enter any name for the App which will appear in the Apps list just like the screenshot in step 1. The changes usually reflect immediately but sometimes may take a few hours till Slack updates their cache.\
![](https://lh7-us.googleusercontent.com/YcBkfw6d2EiP_6aSmdsJENdapm8TlDuxMRGpb0lXtpMd4XBZetPmzJcIGEBisr5XH03Z-GnTPb6a5z6BCpQKHYkiXv8j5N7bmnHTddJBTlPGoLmhAMkxUUTkmQbyJ4s7tfyG1WUKwV1qKBCVZCsebD4)

### Change the Channel Specific Bot Name

This is the name the bot replies as in the specific channel it has been integrated to. By default it is the Workspace name and the channel name.\
![](https://lh7-us.googleusercontent.com/zsVjTIRV9uRWpBz3uGDmZFUKpmdEJE6j9hEUQD0cP2yK25luavdU7OvnoDMzAcDfQT9c3TN_OWg-6qoxuXWSl64vnTO4YWkEgmsWyMNSBdfNZmYJ0_vd0r4BBMNnGKNfZa13gwovq1cvC6X55AGiAk8)

We can change this directly in our database upon request or you can follow the below instructions to change it yourself.

{% hint style="info" %}
The change will take effect immediately on all new messages and won't affect past messages.
{% endhint %}

1. Log into Gooey.AI with the account that added the bot integration to your Slack workspace.&#x20;
2. Go to the Copilot Recipe [Integration Tab](https://gooey.ai/copilot/integrations/), find your integration and expand the “Slack Settings” by clicking on them:\
   ![](https://lh7-us.googleusercontent.com/BsZW_PwSksf41HheGL8BYu4BKcIIiq6wFlEmnN1tVhxJcWgJ4nmUToUvLArwO8XIOuwAtx5k5xuft16QA-6vY5Os6SmlcfaqjYdNp9a7hvQb5IdrztUYeSUAJ8TyZ5t_GMHiqFv3sYZG5fqEph0eTMQ)
3. Change the name and click “Update”.
4. If you refresh the page, the name should have changed.

### Change the read receipt message

{% hint style="info" %}
The change will take effect immediately on all new messages.
{% endhint %}

1. Log in to Gooey.AI with the account that added the bot integration to your Slack workspace.&#x20;
2. Go to the Copilot Recipe [Integration Tab](https://gooey.ai/copilot/integrations/), find your integration and expand the “Slack Settings” by clicking on them:\
   ![](https://lh7-us.googleusercontent.com/BsZW_PwSksf41HheGL8BYu4BKcIIiq6wFlEmnN1tVhxJcWgJ4nmUToUvLArwO8XIOuwAtx5k5xuft16QA-6vY5Os6SmlcfaqjYdNp9a7hvQb5IdrztUYeSUAJ8TyZ5t_GMHiqFv3sYZG5fqEph0eTMQ)
3. Change the read receipt message and click “Update”.
4. If you refresh the page, the receipt text should have changed.

### Remove the Bot

1. &#x20;In the left bar, find and right-click the app in the Apps list and select 'View app details': \
   ![](https://lh7-us.googleusercontent.com/zFX-jdGwzNfth4GEaW01AiyUAjXAMhA9PgTnsCFhcIOmzP4BB6ZzF5wL5w4QJK4-9fm2fBHK7ZClktjjRcIiJw2jylb4ulgRmXoj0BlzcD5yz7zsJHMhIPvTC-kux590bjLG_8hgwcLWX0g5KYBcMt4)
2. Click "Configuration":\
   ![](https://lh7-us.googleusercontent.com/CdtnYMTHURPFPLkkWAjEpzYZl9gk0G261tmQSWEUHZjhFaypCPovUMaKhnNSKKmDr78S3IytnKjYK7uEP3XgERLEcWqBctW1wnzciWHNHHREmBFu5cc9Krecdi90iznlXW9ySPu5_HnqJqCPyuSC_1s)
3. Scroll down to "Remove App" and click "Remove App":\
   ![](https://lh7-us.googleusercontent.com/5nR9xU1la-tDD5Dw1r6TI8pM6asbR-tqDUy0LEjliALJ5gMz2StKhggC03RgX_scDZFRQ37u87jxBCT5qLoV0GnfwfJMrEqyCqyybOq5_cX51-D9cf5Sq31NGZaPzmMQYUOcfvVSArDjRG7kUwBXyR4)

{% hint style="info" %}
Once you’ve removed the copilot app from your workspace, if you ever want to add it or another copilot bot back, you’ll need to click “Add to Workspace” on the integrations page again even though the integration/channel seems to appear in the integrations list. Follow instructions here: [Adding the Copilot Bot to a Slack Workspace](deploy-to-slack.md#adding-the-copilot-bot-to-a-slack-workspace).
{% endhint %}

## Siri Integration

We have experimental Siri support through IOS shortcuts. This will allow you to chat back and forth with any Slack copilot integration verbally via Siri and import conversations into Slack for details.

### Install Siri Integration

1. Install the [Siri Shortcut](https://www.icloud.com/shortcuts/2f158bbcf7644c2aaadc4d11c9180272) by clicking the link on an iPhone (Mac and iPad are not tested).&#x20;
2. Activate the Shortcut by clicking on it or by telling Siri “Start copilot” verbally.
3. The first time, you’ll need to give the shortcut multiple permissions (select “Always allow” on all these to not be prompted again). You will also need to login to your Slack Workspace which requires knowing its URL. This can be found by opening your Slack Workspace and clicking on its icon in the upper left corner. It should be right under the name (in this example it is “gooeyai.slack.com”):\
   ![](https://lh7-us.googleusercontent.com/gcTbTcKU8vrWS6lGBIdR3e9wMM9ebAdqiFGXYfGl5SqH1kJfCWx1-B6Gx_fsjpjfXauNS4OsaUMMUG4DaYUXca1mUxGZk417vW6VCiybIwWq_Bq9wkkHGTSOjOv16GL4bITQshuWTR0bGhkfa3Ch13g)
4. For convenience, you can now add the shortcut to the home screen, lock screen or (iPhone 15+) assign it to your action button. Activating with Siri directly will always work too.

### Add to Home Screen

1. Open your “Shortcuts” app:\
   ![](https://lh7-us.googleusercontent.com/qeCAvLzxvImIoKTS5cWxoe_W87H-uFM4sE6C8Jq7kMb6dnNzFRYwYg-86l8QuQNaI3gsJgYGO83QrHjHXrM2Em0ME8eYPQy1_1rIEBEeMCtYwJlptMTmLg3uubIhmVgriL0UnwOkGmJRj50ggEzpha8)
2. Identify the copilot shortcut (top left orange box in below screenshot):\
   ![](https://lh7-us.googleusercontent.com/nHzvG6AVbD221M0hZ6z_eXvHRcZU3vkLEUW1Qs9ObNllOYul2ovdLTXHOGMH6rkQ0ZQ1m1AqEd4nsVnhhWtBYJvBEuqc43lBT6_xk_B3srl4tO9KMHBME6z_zaO1n9Wq-da0goaha39aSuUxcpBLkpE)
3. Hold down on it to open the context menu:\
   ![](https://lh7-us.googleusercontent.com/98Ua9ke8UVU1ZjhvW-lxPATgdFl1rzNZj_T5u5frsutJMIMkD2beF-rMBSQbfsrp4--Z1ZmdZ26xsgVFOYEIlMO545ZvTu7LqgF-OSHSbcIi2EmAGQevovEjvtAzfJsh0kR6jR_9GWAC5IbStUfF_nQ)
4. Select “Information” (3rd option) from the context menu:\
   ![](https://lh7-us.googleusercontent.com/GqfeQus7OGP2bUUcK5Oe7MQxhWLZSJSjjZjf1rpiCrY4c8nXYvMxKGUZr6OTQI-KfSyXVrlEzmf787GE4AKoGMV7LQK9fzHcq_qPk_WFz_FCw_PJHcXpePLpJ5fcJtVsZaEQKSxjd-DZfuuln17ByOo)
5. Top option will add the shortcut to the home screen.

### Add to Lock Screen

1. Unlock your iPhone and tap and hold on to the lock screen to go into editing mode.\
   ![iPhone lock screen screenshot](https://lh7-us.googleusercontent.com/q8aC34wARfiGaquw3qkwlB5VUDfA4bbkC4ocfGKzDFcQKBgcIHt3n-XRsmcbw756Uqne3GqCCsryZL-E1WTHmVC6VbU5JmSucbtqhJRaiF3tcA7-zQOBbmsNrc-kgR6EzHvXEIw7P-vGKOdRG7g1NdY)
2. Tap the “Customize” button and choose the “Lock Screen” option.\
   ![iPhone lock screen customize option screenshot](https://lh7-us.googleusercontent.com/tPhNZJnHBbnuHcLb8VO79XQ8Pc85KM876XL8HMhWsB_75ibpbzQor9pVDVw1EXeMCU_dCPr-ZKgkBqqa-5t2T4AlXPiH2e_nbhtYsnc4hI8u0T6hJYIV8oRDT4NBuqsjqtl6plOiyGfOpCHLib-lPmY)
3. Tap on “Add Widgets” and scroll down to pick Shortcuts.\
   ![iPhone add widget screen screenshot](https://lh7-us.googleusercontent.com/A1mmcVAk3JbV8sSwROd-4HUmyvp0xatLfAI8X9p6DRYM8aB3VaFa75OMtj3fl-VtiFVWTWJDhn5g0Kws_Lqtaqb-QHA1zvur1ORKmq9tjhjUpirAiKlVBC0DGUMpGONs5pOkyOv8Z1weyt1Zk86oVBU)
4. Tap on the widget to add it to the lock screen. Tap the widget in the widget area to customize it.\
   ![customize widget screenshot](https://lh7-us.googleusercontent.com/uZmzUOS-q3VYlhd3bfxOgy2SvqcgrxX70SYMfu9gM4UPT2j_jbcP3GtZHo9fSpQkdGP259FJtpClE_eG93ye2YS4BKZ22YmYjqqDqZC0dfx8VsIf2aM1actuSAu17M-YcVx74gV1uDFVJgZGSGkxbIk)
5. Select the “Copilot” shortcut.\
   ![](https://lh7-us.googleusercontent.com/wYb0BBb9mehQG6uFB2-R4Q0GuvUhMwhGThqErkq5oblI_Mh4aYop-szYDiSBa8CHwm3_mJd7Wga2Az_-LdtHEjAC6HI_AKoL0rGVfJgiaBIcnNUwJnY9pqHIuZTM3sN7ozi0g353D_a3z_NlFzRxbGM)
6. Tap the cross button and then the “Done” button to save changes.\
   ![saving lock screen customization](https://lh7-us.googleusercontent.com/RP7GmDm4KSc5UbyMhztkqCUHw4vGc87yxbeVZenpAnN_UiSGhbA_PvWWj06_RtX4-H7x3Ccid40wd5fNq2BzsuyQoSqBoIa8qGoFmU3H4N37VxKxWrLbg2m5vXfiiN4svADRCfOmDaLeE4vWDLk_qSE)
7. The shortcut will now show up on the lock screen and can be clicked.\
   ![](https://lh7-us.googleusercontent.com/1XiXT8e2ZwHkKtFeXPeWeE6wLvzka1cU6p_QC2Ah2O-pn56lpKiOc8Tnwb8fEuZpPbRuzpUARIsoYSntzBjHAZApLfZFOMXcA9Yj9USS5azwmsIOfzN7G-1nr-JyYp7aQRWslDVr-Yy0Ix8yBoy5nZU)

## Notes

* The bot currently responds to [Slack Audio](https://slack.com/help/articles/4406235165587-Create-audio-and-video-clips-in-Slack), regular text messages and video messages.
* The bot can respond with text, audio, and/or video if you select those options in the run settings. Check the other [Copilot Guides](../copilot/).
* Don’t try to reset your message history at this point. This is handled automatically by the chatbot logic. Resetting manually will result in all feedback being lost.

## Changelog

v0.0.1 - 8/7/2023 PST

* Basic add integration functionality on gooey.ai/copilot/integrations
* Respond to text and audio
* Custom name for each channel, can only be edited in db
* Reply with text
* Supports collecting feedback

v1.0.0 - 8/8/2023 PST&#x20;

* Works for private channels
* The bot can send back audio and video messages
* Adding the bot to a Slack workspace has been simplified (no need to @invite it if the user is a member of the channel already)
* Reconnect to make the botname match the title of the run/example
* Adding the bot again overwrites so deletion is fine
* To use the new features, the App must be re[added to Slack](deploy-to-slack.md#adding-the-copilot-bot-to-a-slack-workspace)

v1.1.0 - 8/14/2023 PST&#x20;

* Added read receipts
* The read receipt message can be configured on the integration page

v1.2.0 - 8/19/2023 PST \[Actively Deployed]

* Personal channels for private conversations (these have separate conversation histories and messages happen top level instead of in replies)
* Easier channel specific name change
* Better display name in integration page (includes channel and workspace)
* Supports video messages
* To use the new features, the App must be re[added to Slack](deploy-to-slack.md#adding-the-copilot-bot-to-a-slack-workspace)
