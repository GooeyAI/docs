---
icon: clock-rotate-left
---

# Changelog

All notable changes to this project will be documented in this file. It keeps track of changes to the GooeyAI repository - [gooey-server](https://github.com/gooeyAI/gooey-server) and other changes to the [Documentation](https://docs.gooey.ai/) and the [Gooey.AI](https://gooey.ai/) website.&#x20;

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## 30-April-2026

**Added**

* [Stop button to cancel in-progress runs](https://github.com/GooeyAI/gooey-server/commit/7395eda4cf76b59cce735ba945d6435c8c7d1037)
* [Immediately revoke background task when a run is stopped](https://github.com/GooeyAI/gooey-server/commit/998aaa1c38410e855fb9b59c1dfedf1546ee1719)

**Fixed**

* [Show globe icon on share button for public workflows](https://github.com/GooeyAI/gooey-server/commit/dacc414863371276c55f16073f04be97ef81e3ed)
* [Show sharing level in workflow search results](https://github.com/GooeyAI/gooey-server/commit/31fdd0f54df08d3fe4ae0369a566e6e74002dcbf)

## 29-April-2026

**Fixed**

* [Prevent LiveKit DTMF and bot session overlap in voice deployments](https://github.com/GooeyAI/gooey-server/commit/4d631079d16ed3b39380261f12cd0efb8f61bf18)
* [Resolve conflicting CSS styles](https://github.com/GooeyAI/gooey-server/commit/3ac2c5e65293efff2786d2e22679308af23b0c39)

## 28-April-2026

**Added**

* [Dynamic error messages when a run fails due to insufficient credits](https://github.com/GooeyAI/gooey-server/commit/8a751dbd3a82621339c28b79bb6d492ac8ed00b6)

**Fixed**

* [Preserve playable video instead of showing thumbnails in full output](https://github.com/GooeyAI/gooey-server/commit/78f26503baca9acfce45e8f5d2ed22233efa1d7d)
* [Re-upload safety and metadata refresh for file blobs](https://github.com/GooeyAI/gooey-server/commit/80bad08926acf25fd3726652313dd436c52beacd)
* [Update contact URL from help.gooey.ai to gooey.ai](https://github.com/GooeyAI/gooey-server/commit/34300a8be8416536d3cd38d7fa5655534a323219)
* [Correct InsufficientCredits error price reporting](https://github.com/GooeyAI/gooey-server/commit/fb514cfb87b82897ef8f190277baef771ba9c1ce)
* [Fix LiveKit import and duplicate delete() call](https://github.com/GooeyAI/gooey-server/commit/02b443874980cfd32258547273fcbca5acea080b)

## 27-April-2026

**Added**

* [Gemini Live 3.1 support in LiveKit Voice deployments](https://github.com/GooeyAI/gooey-server/commit/f262feed11fad4c3c2dec84a875e528e3a6768fe)

**Fixed**

* [Handle Gemini 3.1 initial greeting correctly with session.say](https://github.com/GooeyAI/gooey-server/commit/31e9167b27a31a7307cd44c419ddda13ddbd13cd)
* [Add prompt validation in Bulk Eval to ensure user input is provided](https://github.com/GooeyAI/gooey-server/commit/9e15ad075f718e894dbc09971cf767a8725eb394)

## 23-April-2026

**Added**

* [Deploy Workflow as an LLM Tool, with WhatsApp country code selector](https://github.com/GooeyAI/gooey-server/commit/1f21165f4288ded57bce01f53613f8f7a3b13a98)

**Fixed**

* [Deployment no longer duplicates the published run before validating Telegram bot token](https://github.com/GooeyAI/gooey-server/commit/7d1ecb814f2014354d57afb709124e4d6c2b553b)
* [Fix "last saved version" link in the integrations tab](https://github.com/GooeyAI/gooey-server/commit/7d1ecb814f2014354d57afb709124e4d6c2b553b)

## 22-April-2026

**Added**

* [GPT Image 2 model support](https://github.com/GooeyAI/gooey-server/commit/0f439a4e0e3e1d4ddaab0c061afd1d71b3b09773)

## 21-April-2026

**Added**

* [Code editor for Bulk Eval prompts, graph captions, and "lower is better" grading option](https://github.com/GooeyAI/gooey-server/commit/bafeb119b2124567726af992b5e54d884358e54f)

## 20-April-2026

**Added**

* [Dynamic LLM tool search via dynamicLLMToolLoader](https://github.com/GooeyAI/gooey-server/commit/be2185ee7881ec205879a9a1a3b899156e2aa7d1)

**Fixed**

* [Video and audio model enum schema generator](https://github.com/GooeyAI/gooey-server/commit/c982d7364eb4154ab3f4a13a51703813b9e3547e)

## 16-April-2026

**Fixed**

* [Properly center "Processing…" text on the processing page](https://github.com/GooeyAI/gooey-server/commit/c1ed099625857b22a4df46ecee8c4be7ea29babf)
* [Current plan card rendering on mobile view](https://github.com/GooeyAI/gooey-server/commit/a66e824a26696a91fc1ea4499a89969d75528c3e)
* [Downgrade Pro plan correctly and show downgrade info for tier](https://github.com/GooeyAI/gooey-server/commit/2f6ca78f04de57b60a860083e44940caa41c2634)
* [Clear all pending Stripe subscription changes before cancellation](https://github.com/GooeyAI/gooey-server/commit/267181c09d9ee383fa91d98469f4dd175a1b1368)
* [Don't send low balance email for Team workspaces](https://github.com/GooeyAI/gooey-server/commit/8113f7682bdef947be0e775a7cd5c28b3d581eea)
* [Default seat count to next highest option when not in plan options](https://github.com/GooeyAI/gooey-server/commit/d21a74d61f089c461b3a7d68b5ad67c51f85da11)
* [PayPal users can now see seat selection](https://github.com/GooeyAI/gooey-server/commit/c20aacd2c00776224fef6758d192ceceba16b082)
* [Clear pending Stripe changes before upgrade or downgrade](https://github.com/GooeyAI/gooey-server/commit/f19b6633179bff44dfe5045f37f473a9fa3e8ab7)

## 14-April-2026

**Added**

* ["Last login" column in the workspace members view](https://github.com/GooeyAI/gooey-server/commit/08ac231bb13599446cc5456883aca3a89f25f46b)

**Fixed**

* [Invite accept logic now correctly creates admin seats](https://github.com/GooeyAI/gooey-server/commit/cdcfedfa55dfadd3de3343f32cd34a0bde2b001e)
* [Payment method detach now called before redirect](https://github.com/GooeyAI/gooey-server/commit/017fade77922a582c2e0acde4ebbcc418eb208c5)

## 10-April-2026

**Fixed**

* [Files uploaded via API are now correctly marked as user-uploaded](https://github.com/GooeyAI/gooey-server/commit/23c80ec1b599f9e7a4485ccc2941e504d29a32d4)

## 07-April-2026

**Fixed**

* [Show "Upgrade to invite members" only to admins on a free team](https://github.com/GooeyAI/gooey-server/commit/378337ec395cf666c5cdebfb0dfd92a310c3fcd0)
* [Schedule plan change correctly for all downgrades](https://github.com/GooeyAI/gooey-server/commit/1c26d79fca3e7649214fe12805996821906a87b4)
* [Rounding error in Pro plan pricing](https://github.com/GooeyAI/gooey-server/commit/f23dabe79d8c40f385f69b7cfe32a23b3fe3b4c2)

## 05-April-2026

**Fixed**

* [Stale workspace no longer passed to auto-assign team members](https://github.com/GooeyAI/gooey-server/commit/d283a505faba533937ffa85e702ba75a1e85be47)

## 02-April-2026

**Fixed**

* [Balance correctly set to zero when cancelling a subscription](https://github.com/GooeyAI/gooey-server/commit/2cc6c681bb228d2827d6406c6bf1592adb6cd907)
* [Redirect to Stripe correctly after creating a workspace](https://github.com/GooeyAI/gooey-server/commit/55639cc6bee5c98d41fd4d6181b9a4ed495267f5)

## 01-April-2026

**Added**

* [Show "Upgrade to invite members" prompt on free workspace Members tab](https://github.com/GooeyAI/gooey-server/commit/f16a4119a4bb4cbef5940a6edb56379896c1d599)
* [Link to team plans from the Create Workspace popup](https://github.com/GooeyAI/gooey-server/commit/00b61b68d2969905b3754b97dad60876cf6eb813)

**Fixed**

* [Seats are now unassigned when members are soft-deleted](https://github.com/GooeyAI/gooey-server/commit/acbaf35c941ad84529b41bfee3f5cf1253333964)
* [Invite option now only shown in workflow-share dialog for paid workspaces](https://github.com/GooeyAI/gooey-server/commit/a497dfc241162ca8a7ed1395441a827182c4c927)
* [Prevent non-team/enterprise workspaces from sending invites](https://github.com/GooeyAI/gooey-server/commit/3d5712152cacfcd3e5adce634d3cb8be5c6307e0)

## 30-March-2026

**Added**

* [Message structure transformation for Fireworks chat](https://github.com/GooeyAI/gooey-server/commit/09b357657bb0f92b6f92f57b82208fdd4b308ca8)
* [Pre-create file upload entries before background task runs to prevent data loss](https://github.com/GooeyAI/gooey-server/commit/e602bfcc4b031c35c969224b0fb330bc2b8b31b8)

**Fixed**

* [Telegram blocking behaviour with no timeout; added Telegram markdown renderer](https://github.com/GooeyAI/gooey-server/commit/033d2dfbda7a7387af6d2e1e5fbc3e559b1a1972)
* [`final_search_query` response\_format\_type to support `json_object`](https://github.com/GooeyAI/gooey-server/commit/e18015df297b4cf0f03237986625aa7cf160b3dd)

## 28-March-2026

**Changed**

* [LLM and video model sorting by priority desc, then reverse alphabetically](https://github.com/GooeyAI/gooey-server/commit/bea4c785e0e9c5a06468649da4ae6af679550591)
* [Creator priority in frontend model ordering](https://github.com/GooeyAI/gooey-server/commit/7a5627f0315afac227be3b940c68214cb1659f84)

## 27-March-2026

**Fixed**

* [Duplicate source permissions enforcement](https://github.com/GooeyAI/gooey-server/commit/15611068d529f8519c067cbef44eec7f4154b49e)
* [ConnectChoice image URLs in VideoBots](https://github.com/GooeyAI/gooey-server/commit/7c4d38e0a3a572c4d14fc4347597bb51be0a3796)

## 26-March-2026

**Added**

* [AI model creators with creator icons in model selectors](https://github.com/GooeyAI/gooey-server/commit/cd93655e018e338f69f1a804e61949ea169b0e03)
* [Private-chat streaming via `sendMessageDraft`](https://github.com/GooeyAI/gooey-server/commit/1b5048b444dec303e3c3de283b53ca028c1bf1ab)

## 25-March-2026

**Added**

* [Intron ASR integration](https://github.com/GooeyAI/gooey-server/commit/622cde9cbe6421179fd8c74ada11e700921cd1dd)
* [Video model priority ordering](https://github.com/GooeyAI/gooey-server/commit/92950f0319800d0533f035b90c279b50125d373d)
* [Auto-register `/new` command during Telegram bot setup](https://github.com/GooeyAI/gooey-server/commit/1984647f2bb5cbd2bf4526606fe62bbfff4e0190)

**Fixed**

* [Bulk eval first-group flush](https://github.com/GooeyAI/gooey-server/commit/a0744348993955ed47c0f5545ed970852c12c797)

## 24-March-2026

**Added**

* [Inline widget bootstrap; hydrate builder sessions from saved-run conversation data](https://github.com/GooeyAI/gooey-server/commit/1153687372606788e1838b464bbba8a74b872fe6)

**Fixed**

* [Faster query for getting child builder run from parent](https://github.com/GooeyAI/gooey-server/commit/b95581f0fbad90247ef3788c2a4bdb51da74384d)

## 20-March-2026

**Added**

* [Checkbox for `showToolCalls` in web widget integration](https://github.com/GooeyAI/gooey-server/commit/a6a8329e4eb756b377f82569fcc8a3da3b51b8aa)

**Fixed**

* [Store `parent_builder_saved_run` as FK; update Gooey Builder messages on navigation](https://github.com/GooeyAI/gooey-server/commit/6f1d4b88a59511b89f41a0376a0caafaf2037546)
* [Max-width on global `img` tag to prevent overflow in recipe descriptions](https://github.com/GooeyAI/gooey-server/commit/29e877389f53f03dde1d201fae1d0c892784a2f3)

## 17-March-2026

**Added**

* [Faster streaming on Telegram](https://github.com/GooeyAI/gooey-server/commit/509218a2aec815468f74eb976fdf024a2ccedaf4)
* [Paid-only audio/video models](https://github.com/GooeyAI/gooey-server/commit/b5dd84c2c2f7a318299fb1aa028b0aefe02f4467)

**Fixed**

* [Telegram help link updated to Gooey docs](https://github.com/GooeyAI/gooey-server/commit/a2b10e917ab193937c634546a17651631e3f47af)
* [Chat completion message conversion for Responses API](https://github.com/GooeyAI/gooey-server/commit/34e69aba67ac1651d49c929f3d28af64956cf65b)

## 12-March-2026

**Added**

* [Telegram bot deployment](https://github.com/GooeyAI/gooey-server/commit/b35e299520ea0386a57e2591a033485c2786af11)

## 11-March-2026

**Added**

* [Gooey Builder: allow pressing buttons without creating a new run](https://github.com/GooeyAI/gooey-server/commit/a0b49204b5e716f39e5169829587220f6d5d4011)

## 10-March-2026

**Added**

* [Country code selection for shared phone numbers in Voice Deployment](https://github.com/GooeyAI/gooey-server/commit/6233b06dcd8fb74b97aa486db3be15ef0d7f2c7f)

**Fixed**

* [Show tool calls only on `/copilot` page by default](https://github.com/GooeyAI/gooey-server/commit/e770175d0491c4001a06b5b9aa8d15ffb52cd13a)

## 06-March-2026

**Added**

* [Stream `final_prompt` chunks in bots API to render tool calls in web widget](https://github.com/GooeyAI/gooey-server/commit/9f76ee664a61869aa41f9b773c93c85fd66f023f)

**Fixed**

* [Auto-remove unused template variables](https://github.com/GooeyAI/gooey-server/commit/fe6286d25cbd783c36b7741c4c7a6eda7b7fd669)

## 04-March-2026

**Added**

* [Privacy Policy section and Code of Conduct to README](https://github.com/GooeyAI/gooey-server/commit/d918e9e5ff04853b87f99f65008f33a64eda8c73)
* [License updated to Apache 2.0, copyright updated to 2026](https://github.com/GooeyAI/gooey-server/commit/d618176c87cee6c208e66779c4b669a37429b29d)

## 01-March-2026

**Added**

* [Voxtral ASR support](https://github.com/GooeyAI/gooey-server/commit/ad46112d1dc8301376d9a69c421a775c8f4e32d3)
* [Latest Mistral embed, OCR, and LLM models](https://github.com/GooeyAI/gooey-server/commit/f3ed03b945b342688f4f68abfe905ac44a57fd6b)

**Fixed**

* [Mistral references chunks handling](https://github.com/GooeyAI/gooey-server/commit/1f50955aae934a129972254daecb25790bad27e4)
* [Google Sheet extraction with document model](https://github.com/GooeyAI/gooey-server/commit/5f020f3ed01b7ad9dded27e3928dd1470abdcfa1)

## 27-February-2026

**Fixed**

* [Guard `query_vespa` against empty/invisible search queries — prevent Vespa 400 "NullItem" errors](https://github.com/GooeyAI/gooey-server/commit/7422aef292c64aef04c7c105181977b55ed859de)
* [Handle `None` keyword\_query in `query_vespa`](https://github.com/GooeyAI/gooey-server/commit/586abcf4200e7f0436360307d32d1fd2d0eb7f9d)

## 25-February-2026

**Added**

* [Batch memory updates from Python/JS functions](https://github.com/GooeyAI/gooey-server/commit/4e33b7a2ba8d51ddf6ac2a70c5a57c42dedc22f1)

## 21-February-2026

**Fixed**

* [Array columns handling in evals](https://github.com/GooeyAI/gooey-server/commit/7135cb66090ea658be2c88d6e96de35bf75a3f56)

## 20-February-2026

**Fixed**

* [Bot-builder videogen inputs schema](https://github.com/GooeyAI/gooey-server/commit/71f2f5a3b0d9af32714d508691b035810fdf4291)

## 18-February-2026

**Fixed**

* [Padding issues; render audio input/output in Copilot; move history filter widget out of base.py](https://github.com/GooeyAI/gooey-server/commit/5f699b2dea7829158ad37c204c2f707594a62e7b)
* [History filter not shown for non-logged-in users](https://github.com/GooeyAI/gooey-server/commit/bf602e7b24d14156b13d621c696f1edc5150ec8d)

## 14-February-2026

**Fixed**

* [Composio "Connect & Grant Access" button redirect](https://github.com/GooeyAI/gooey-server/commit/8ffd1db24ca0bd33a75e399301647568e68ad89e)

## 12-February-2026

**Added**

* [Per-person history on history page](https://github.com/GooeyAI/gooey-server/commit/f70af54dd7b74601d380f1aa1beeff48d797336f)

**Fixed**

* [Preserve whitespace when streaming text](https://github.com/GooeyAI/gooey-server/commit/201b65feead809ebc4a81f1a9b5623e419bb25d0)
* [Video history UI and model name display](https://github.com/GooeyAI/gooey-server/commit/469af185ce8424b787bad739482052dd904d0fcc)
* ["Add variable" button incorrectly creating a new function](https://github.com/GooeyAI/gooey-server/commit/6fd9bafaa68b172a617ef376f2ca8b08b8da227c)

## 04-February-2026

**Fixed**

* [DTMF timeout and disconnects in LiveKit agent loop](https://github.com/GooeyAI/gooey-server/commit/b93fde305fdaa33892a822d7095a5a1cb79e7a23)
* [Support for non-Twilio numbers in LiveKit](https://github.com/GooeyAI/gooey-server/commit/dc27039baa3a6b125ada053fdd170310564cd702)
* [Empty photo URL in branding](https://github.com/GooeyAI/gooey-server/commit/889b182d3832a702aaffcf2df27bb31304f1596a)

## 03-February-2026

**Added**

* [Authentication and credit notification email templates; `error_params` field in SavedRun model](https://github.com/GooeyAI/gooey-server/commit/c01015ddf7da3faf1c0306afa90a13aa8c34d939)

**Fixed**

* [Updated credit costs for image generation models](https://github.com/GooeyAI/gooey-server/commit/8e32439b227c8f518a2220c09c8915e9faf406a9)
* [Copilot web widget branding](https://github.com/GooeyAI/gooey-server/commit/bdb293ed20c7161edfc331ea114233d0fe27df0c)
* [Null variables handling in API; null version retrieval in saved workflow](https://github.com/GooeyAI/gooey-server/commit/a0c3241a5aca56e3b072b2687d87318dd1b6f61f)

## 30-January-2026

**Added**

* [Private Google Drive file access via Composio auth](https://github.com/GooeyAI/gooey-server/commit/cc5986580cf160d8a970a8cc98dca6253138814c)
* [Support for multiple Google Drive accounts via Composio](https://github.com/GooeyAI/gooey-server/commit/1e4c5623e8f6fadfcfd52b72a83dd8b468cb8cd9)

## 26-January-2026

**Added**

* [SSO login support](https://github.com/GooeyAI/gooey-server/commit/44372a07e86af78762b713e64d7d3056f0d886a6)
* [Draft run created every time Gooey Builder updates state](https://github.com/GooeyAI/gooey-server/commit/4d63ca6c6cece5be50775f6e95ed931746b10867)

## 20-January-2026

**Added**

* [Render video URLs from markdown in WhatsApp](https://github.com/GooeyAI/gooey-server/commit/704970a3c07ac57f63719e7d73a05ae07b4151f1)
* [Thinking summary display in Copilot; stream thinking messages](https://github.com/GooeyAI/gooey-server/commit/6ff3114b0761c733edc99a58254b30b1d09b7526)

## 16-January-2026

**Added**

* [Thinking summary in Copilot](https://github.com/GooeyAI/gooey-server/commit/2bb01a9da759d5aaac4443beeaf34a9e29411ea0)

## 15-January-2026

**Added**

* [LiveKit call recording and transcript](https://github.com/GooeyAI/gooey-server/commit/1488b1ec4e0f129669854f9f295f33d173a08deb)

## 14-January-2026

**Added**

* [Support for OpenAI Responses API](https://github.com/GooeyAI/gooey-server/commit/b4c4e7d6d65a21c506acc4452e387b52667a3b53)

## 12-January-2026

**Added**

* [Custom OpenAPI-based model support in LiveKit](https://github.com/GooeyAI/gooey-server/commit/9b5c3d7996f4787777b9fd586690c8c458eff8d3)

## 02-January-2026

**Fixed**

* [Bot builder photo URL picked from branding](https://github.com/GooeyAI/gooey-server/commit/5fae37c043c4d2bcdf2dc1a6830bb8e99d145b7e)

***

## 19-December-2025

**Fixed**

* [Formatting issue in Gooey Builder](https://github.com/GooeyAI/gooey-server/commit/4a1af2b4b7487a135b25855c6ea85aaf32d3f010)

## 18-December-2025

**Fixed**

* [Progress bar z-index order](https://github.com/GooeyAI/gooey-server/commit/83d48acaf4094defef561d97450afa8fd2d4665a)

## 28-November-2025

Changed

* [Videogen schema: add support for non-string enums](https://github.com/GooeyAI/gooey-server/commit/6282d675d551c6393be0b0eb7c90fd1e4777214b)

## 26-November-2025

Changed

* [Use audio input capability for Gemini LLMs](https://github.com/GooeyAI/gooey-server/commit/7a610f536b25771f1d42c6987db59c26546bfe46)

Fixed

* [Only render updated\_at/generated timestamp once](https://github.com/GooeyAI/gooey-server/commit/a683bba6e945c2831bcb4a2881a03fb142c13c5e)

## 25-November-2025

Changed

* [Move MMS TTS & Omnilingual models](https://github.com/GooeyAI/gooey-server/commit/b6936ff51eb0ddfcd5b8437d179e624a552f9b77)

## 21-November-2025

Added

* [Meta Omnilingual ASR model](https://github.com/GooeyAI/gooey-server/commit/ebc19e8b827600d4fb1cb0a2c62b29c8dcbd12b9)

## 19-November-2025

Added

* [Support for GPT-5.1](https://github.com/GooeyAI/gooey-server/commit/79aa874ae1d32308756b8c90bac9298149d401ad)
* [Support for Gemini 3 Pro preview](https://github.com/GooeyAI/gooey-server/commit/135c6bc6447b993ec1b959ca9d56ae2ef8919a22)

## 18-November-2025

Fixed

* [Make modal import lazy](https://github.com/GooeyAI/gooey-server/commit/e4c9a472253833a22105c5e50b64edfb9039bc1a)

## 29-September-2025

_Fixed_

* [cleaner filter for removing image-url content chunks](https://github.com/GooeyAI/gooey-server/commit/e4339f693f6ae233370a62f408019953225e0246)

## 25-September-2025

_Fixed_

* [remove rank from order\_by when search is empty](https://github.com/GooeyAI/gooey-server/commit/9b808f0debd425ab1fc037fc8579002a37282c12)

## 24-September-2025

_Added_

* [render pricing notes and example preview on video gen](https://github.com/GooeyAI/gooey-server/commit/45ef6e6bcc1a1d0965c2ad8b0bb6f158ee54f69d)

## 18-September-2025

_Fixed_

* [image input creates invalid API request for apertus model](https://github.com/GooeyAI/gooey-server/commit/d672282380c5b2995ddddb113e10cfe6a41b3024)

## 16-September-2025

_Added_

* [implement LiveKit voice agent with Twilio integration](https://github.com/GooeyAI/gooey-server/commit/43dcc31430920628941e669d84d733c82071746e)

## 15-September-2025

_Added_

* [add support for Nano Banana](https://github.com/GooeyAI/gooey-server/commit/e10c19e3526c8ae3569c7634155718b57ded1612)
* [add explore link in header](https://github.com/GooeyAI/gooey-server/commit/bd158e66da29c177029a7b16bb73e02054055534)

## 11-September-2025

_Added_

* [add support for SwissAI Apertus LLM](https://github.com/GooeyAI/gooey-server/commit/607f57c15526a4d5ca329ec167af7216dab5dd78)

## 25-August-2025

**Added**

* [version stats](https://github.com/GooeyAI/gooey-server/commit/ae6ad719aa8580ff3654502612e677957011f365)

## 22-August-2025

**Added**

* [implement reasoning\_effort for openai, claude and gemini](https://github.com/GooeyAI/gooey-server/commit/db8e9fc259e35cfd8d922635f4db0d043a786c97)

## 21-August-2025

**Added**

* [add mbaza asr model](https://github.com/GooeyAI/gooey-server/commit/b3f664741127a40a642e796b683733a742b6019a)

## 20-August-2025

**Added**

* [combined analysis plot with correct data & timezone selector](https://github.com/GooeyAI/gooey-server/commit/83517ff46f6522f1472165e2e936625e59e8ef33)

## 18-August-2025

**Added**

* [add gemini 2.5 flash lite](https://github.com/GooeyAI/gooey-server/commit/d0a8b00225c38a5286c8ee5679345b13cea59d37)

## 14-August-2025

**Added**

* [bulk runs on copilot](https://github.com/GooeyAI/gooey-server/commit/d89fb3ae4f4610573fd19ede64a6e9f056e2f076)

## 13-August-2025

**Added**

* [Aspect ratio icons and functionality to DeforumSDPage](https://github.com/GooeyAI/gooey-server/commit/0b3d58d38375408825df417b9d6b77052c3c55d6)
* [Support for reasoning\_effort for OpenAI and Gemini thinking models](https://github.com/GooeyAI/gooey-server/commit/df6c25efc905e6f9321b79baba00556dd815ff5b)

## 12-August-2025

**Added**

* [Show "Open Workspace" on public team page for non-admins](https://github.com/GooeyAI/gooey-server/commit/e66d9a26188547bf459851cdb77c4ae27be07d4c)

## 09-August-2025

**Added**

* [Added GPT-5 Models](https://github.com/GooeyAI/gooey-server/commit/55d181c6cb996b99e6a21e31b5bcab841cfe709d)

## 22-July-2025

**Added**

* [Added Flux.1 Kontext \[pro\]](https://github.com/GooeyAI/gooey-server/pull/736)

## 08-May-2025

**Added**

* [Added o3, o4-mini, 4.1, 4.1-mini, and 4.1-nano](https://github.com/GooeyAI/gooey-server/pull/646)
* [Added gpt 2.5 flash preview model](https://github.com/GooeyAI/gooey-server/pull/655)
* ["Help guide" button in workflow header](https://github.com/GooeyAI/gooey-server/pull/657)

**Changed**

* [Clearer wording on share dialog](https://github.com/GooeyAI/gooey-server/pull/652)
* [Changed placement for visibility on the workflow list](https://github.com/GooeyAI/gooey-server/pull/652)
* [Changed workflow list to show workspaces name in front of user pill](https://github.com/GooeyAI/gooey-server/pull/656)

**Fixed**

* [Bugfix for Gemini 2.5 pro preview: lower bound for max tokens to accommodate thinking tokens](https://github.com/GooeyAI/gooey-server/pull/653)

## 18-Nov-2024

**Fixed**

_UX:_

* Removed the signout button from the profiles page (now we have the profile dropdown) - ([commit](https://github.com/GooeyAI/gooey-server/commit/2404a1e97eb54e8669024896f661033c2c4ce7f8))
* Use an icon with more click-space for more options in the menu
* Fixed bug where the share button disappears from a saved run - ([commit](https://github.com/GooeyAI/gooey-server/commit/e0a9119b0ccab0ef68d63c11e53af4d1cc4f2786))
* Support change notes for saved runs&#x20;
* Better button placement in version history&#x20;

**Added**

_Workspaces \[beta]:_&#x20;

* Breadcrumbs in workspace>author style ([commit](https://github.com/GooeyAI/gooey-server/commit/0d93d32720033f9f8a07f417904e803824d1feaa))&#x20;
* Better invitation email text ([commit](https://github.com/GooeyAI/gooey-server/commit/2c94b7c321aaabddf3ebb4a131dc2853eccefb32))&#x20;
* Better text labels for account pages ([commit](https://github.com/GooeyAI/gooey-server/commit/40c02993e8289880643293da8b16964109083aa1))
* Show workspace selector in "Save" dialog ([commit](https://github.com/GooeyAI/gooey-server/commit/557184bd6e1fce0d7e3583e6fd9bfe8bdce75e55))
* Added URL fragments to the reference links for improved redirection to specific sections on cited webpages [#502](https://github.com/GooeyAI/gooey-server/pull/502)

## 11-Oct-2024

**Fixed**

* Render correct run cost estimate when something on the page changes [#475](https://github.com/GooeyAI/gooey-server/pull/475)

**Added**

* Ability to select LLM on /eval [#472](https://github.com/GooeyAI/gooey-server/pull/472)
* UX improvements to "save as new" / "save" for anon & logged in users ([#453](https://github.com/GooeyAI/gooey-server/pull/453), [#481](https://github.com/GooeyAI/gooey-server/pull/481))
* New "share" dialog for published runs [#453](https://github.com/GooeyAI/gooey-server/pull/453)

## 17-Sep-2024

#### Added

* Beta release of Python SDK - [https://github.com/gooeyai/python-sdk](https://github.com/gooeyai/python-sdk) and [https://pypi.org/project/gooeyai/](https://pypi.org/project/gooeyai/)
* Improve OpenAPI spec to use the standard security scheme definition for Bearer

#### Fixed:

* Bug fix for SERP search location when set to st

## 11-Sep-2024

#### Added

* Updated web widget chat with a [sidebar to contain conversation history](https://github.com/GooeyAI/gooey-web-widget/commit/0dccc94c36a276fd49c91aa247fdfb2e073b0daa)
* [All error codes are available in the documentation](https://docs.gooey.ai/api-reference/error-codes)

## 03-Sep-2024

#### Added

* [Updated GPT-4o to `gpt-4o-2024-08-06` with support for **16,384 output tokens**](https://github.com/GooeyAI/gooey-server/commit/8274b3d4513ce4fcc63a125f386fd582d24b029c)
* Added support for [Gemini 1.5 Flash](https://deepmind.google/technologies/gemini/flash/) and [ChatGPT-4o models](https://platform.openai.com/docs/models/gpt-4o)
* Support for JSON mode on Gemini 1.5 Pro, Gemini 1.5 Flash, and Claude
  * Try here:  [LLM JSON Output](https://gooey.ai/compare-large-language-models/lesson-plan-json-mode-bfmfw2xqksd7/)

## 28-Aug-2024

#### Added

* [Allow auto-recharge for users without a paid subscription](https://github.com/GooeyAI/gooey-server/commit/bb334bc7314577c6fb13d0c0d6a12e15343ac39a)
* Allow saving payment method after a top-up for easier payments in the future
* Updated meta descriptions for: https://gooey.ai/llm and https://gooey.ai/copilot&#x20;
* [Rate limits page](https://docs.gooey.ai/api-reference/rate-limits)

#### Fixed&#x20;

* [Regression on top-up payments with PayPal](https://github.com/GooeyAI/gooey-server/commit/200d559250b43cebbd02f8c19e9438b64306923f)

## 20-Aug-2024

#### Added

* [**LLM**](https://gooey.ai/compare-large-language-models): Updated [Sarvam](https://www.sarvam.ai/), GPT-4o Mini, [SEA-LION-v2](https://aisingapore.org/aiproducts/sea-lion/). Head over to our Compare LLM Generator to see it in action, [SEA-LION v2](https://gooey.ai/compare-large-language-models/compare-llms-sea-lion-vs-sota-h6anugije1jf/) and [Sarvam](https://gooey.ai/compare-large-language-models/compare-smol-models-ffutnq5io8g4/) available here!
* [**Functions**](https://gooey.ai/functions): Revamped functions editor with an in-built linter.
* [**AI Standards**](https://gooey.ai/standards): Our proposal to the Library of Congress and Rockefeller Foundation on how shared AI workflows can catalyze innovation everywhere.
* [**Impact**](https://gooey.ai/impact): Understand how you can use GenAI for your Impact Organization.

## 14-Aug-2024

#### Added

* **Speech Recognition and Translation**: We have upgraded Seamless M4T to v2. This provides improved ASR for nearly 100 languages. Try it here: [https://gooey.ai/speech/seamless-m4t-v2-hindi-english-g8883e8675gk/](https://gooey.ai/speech/seamless-m4t-v2-hindi-english-g8883e8675gk/)
*   **Copilot:** Enabled "Auto-play responses" in **Copilot** Web Widget Integrations. You can control whether audio/video responses should be auto-played or not. This feature is enabled by default.<br>

    <figure><img src=".gitbook/assets/Auto-play (1).png" alt=""><figcaption></figcaption></figure>

## 8-Aug-2024

#### Added

*   **Lipsync**: We have deployed some improvements around the SadTalker lipsync model

    * more understandable error messages,
    * support for a wider range of image/video resolutions,
    * the ability to not crash on long videos,
    * better support for video inputs overall.

    Here is an example of the improved performance on video input:

_OLD OUTPUT_

{% embed url="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/eef688c8-1dfb-11ef-af8a-02420a000128/gooey.ai%20lipsync.mp4" %}

_NEW OUTPUT_

{% embed url="https://storage.googleapis.com/dara-c1b52.appspot.com/daras_ai/media/1db03ed8-4ecc-11ef-b5a4-02420a000192/gooey.ai%20lipsync.mp4" %}

#### Fixed

* **Lipsync**: bug fixes for short input audio and reference inputs

## 24-Jul-2024

#### Fixed

* Fixed the regression with our eleven labs custom voices support. You should now be able to use your custom 11labs voices using your API key on [https://gooey.ai/compare-text-to-speech-engines](https://gooey.ai/compare-text-to-speech-engines) , [https://gooey.ai/copilot/](https://gooey.ai/copilot/) and [https://gooey.ai/lipsync-maker/](https://gooey.ai/lipsync-maker/)
