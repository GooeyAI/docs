---
icon: clock-rotate-left
---

# Changelog

All notable changes to this project will be documented in this file. It keeps track of changes to the GooeyAI repository - [gooey-server](https://github.com/gooeyAI/gooey-server) and other changes to the [Documentation](https://docs.gooey.ai/) and the [Gooey.AI](https://gooey.ai/) website.&#x20;

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## 29-September-2026

**Fixed**

* [Add a fallback request method for status code 405 in the `_get_media_mimetype` function](https://github.com/GooeyAI/gooey-server/commit/e2d71530efa7f702f624a86e7a6c04d57a882bbb)

## 28-September-2026

**Fixed**

* [Print full traceback for eco cost failures](https://github.com/GooeyAI/gooey-server/commit/738aa745aa5ab90cd86b46fbcedb0f603c763bab)
* [Fix the publish dot on the top bar](https://github.com/GooeyAI/gooey-server/commit/5c140a924e667f501a0f4665bb32ba007c416457)
* [Let the Ask Gooey button wear the mark or nothing at all](https://github.com/GooeyAI/gooey-server/commit/a8eed0e48bda4780ca34a8c14291c80b867cbd5c)

## 25-September-2026

**Added**

* [Show usage in USD instead of credits](https://github.com/GooeyAI/gooey-server/commit/2ee0d0daf9070b6ce37bab44242298d8a28dd389)
* [Custom hover band, tooltip and legend for the usage chart](https://github.com/GooeyAI/gooey-server/commit/e428fe77f8c5b4c796763a75358d2f9acf53a68f)
* [/account/usage page with monthly credit usage by recipe](https://github.com/GooeyAI/gooey-server/commit/90339521a26378a51d658a95b4f2de09103ae7e3)

**Fixed**

* [Harden the eco sheet swipe against interrupts and motion settings](https://github.com/GooeyAI/gooey-server/commit/6da1f804425ef7b2001842ae4309f0597699a1f4)
* [Capture eco cost failures in Sentry](https://github.com/GooeyAI/gooey-server/commit/b3ed12bc5456449dac4933dfc708eb5e641b8e55)

## 24-September-2026

**Added**

* [Swipe the eco cost sheet down to close it](https://github.com/GooeyAI/gooey-server/commit/b270481edcd6c1f0239c16b01335ead120a10a32)
* [Read the turns slider as monthly users at 8 messages a month](https://github.com/GooeyAI/gooey-server/commit/ae761ba98368894dfef9d90f4fca7055a4cafe24)

**Fixed**

* [Centre the eco cost modal vertically on desktop](https://github.com/GooeyAI/gooey-server/commit/0ae4ec96531054727c72a748fd2a39952b684145)
* [Never let an eco cost failure break the page](https://github.com/GooeyAI/gooey-server/commit/b43603bc611977ba626eb909b0e3846d55b395d8)
* [Keep workflows saved after login private](https://github.com/GooeyAI/gooey-server/commit/34fef2733d8c0688c4c05533c294852d0f3d4d13)
* [Keep Bot Builder workflow copies private](https://github.com/GooeyAI/gooey-server/commit/bb6a8898f8424ff8616250d62f32301873b3cb26)
* [Keep duplicated workflows private](https://github.com/GooeyAI/gooey-server/commit/932df1ea542ced6b78ce603b2e15117fb11bb221)
* [Stop the two side tracks insisting on being the same width](https://github.com/GooeyAI/gooey-server/commit/02af5322870ce572199f59c081c1c927300559b3)
* [Measure what the bar wants, not what it was already squeezed into](https://github.com/GooeyAI/gooey-server/commit/1ce3dd16458ce02b2237eddb0093e83e5178817e)
* [Fall back to the workflow's name when no wordmark is sent](https://github.com/GooeyAI/gooey-server/commit/fb77c1eb829f374334a16e782c7c64517a3bfac1)

## 23-September-2026

**Added**

* [Per-run eco cost in the top bar and a cost & environment impact modal](https://github.com/GooeyAI/gooey-server/commit/3869056f3523b95b176949d80221d8227dbc109f)
* [Use datetime + workflow title filenames for all VideoGenPage videos](https://github.com/GooeyAI/gooey-server/commit/ea007c600fb6861956b152030e5726ad91915590)
* [Name agent-generated videos with a UTC timestamp and agent title](https://github.com/GooeyAI/gooey-server/commit/63a5bcbd91c1be758ef07f3a05e29ee542b54077)
* [Allow overriding the filename of re-uploaded fal assets](https://github.com/GooeyAI/gooey-server/commit/7ad349f48ee0bb2d1bdd224d227685b80efe8a66)

**Fixed**

* [Explain low confidence with ecocost's reason codes](https://github.com/GooeyAI/gooey-server/commit/6985875d31b2c94252445706e312b33fd9a3515b)
* [Review fixes, mobile access, and a stable phone layout](https://github.com/GooeyAI/gooey-server/commit/cfb179993eea5b4f458b6da8b9e7adccd909babb)
* [Keep the file extension when a fal filename stem contains a dot](https://github.com/GooeyAI/gooey-server/commit/afcf18dc28ca8f324517eb4e8f097d43fe35ddd0)

## 22-September-2026

**Fixed**

* [Deferred pane shouldn't load after its switched away from](https://github.com/GooeyAI/gooey-server/commit/8ca902da27ab5c46cefb2e281387108d9f9a6f0d)

## 21-September-2026

**Added**

* [Let sliders be empty and unset optional model fields](https://github.com/GooeyAI/gooey-server/commit/d42a3e89eea1c4f3932cd136831e40056c3d8180)
* [Add erase button to image/video model sliders](https://github.com/GooeyAI/gooey-server/commit/dee0875fc72e37fd0e378191c67ffa40c6e98bb7)
* [Shed the bar's labels by measuring, not by breakpoint](https://github.com/GooeyAI/gooey-server/commit/147a32f808ae480be1e291a30076746ae32ab27c)

**Fixed**

* [Run safety checker on the rendered prompt](https://github.com/GooeyAI/gooey-server/commit/a0bfcd74d2e7a902b2d694ed0550ff50f68e2c6f)
* [Make the fully-labelled bar prove it has room for one more chip](https://github.com/GooeyAI/gooey-server/commit/ae1a664a84fde346ee5a05b0d37ea74699684594)
* [Pair the view-transition name to the transitioning instance, not a startup counter](https://github.com/GooeyAI/gooey-server/commit/78257b49646c879e7c2f71dcebd92fd8dcbe1d11)
* [Stop a tooltip outliving the control it points at](https://github.com/GooeyAI/gooey-server/commit/85e3853b633b58ce417ff947884713a5eb818b56)

## 19-September-2026

**Added**

* [Hold tooltips back 1.2s](https://github.com/GooeyAI/gooey-server/commit/d44ef37fed25bf2407ec52f8dc0b34eb29015306)
* [Name the bar's controls with the tooltip v2 uses elsewhere](https://github.com/GooeyAI/gooey-server/commit/fae56663fd359f52029e1728c0bc79747a9dad5b)

**Fixed**

* [Let a tooltip out of the box that laid out the thing it points at](https://github.com/GooeyAI/gooey-server/commit/d65ae2c8e194de2084ca56a6f2cbd6fd637fdf36)
* [Gate the bar's labels on a 1440px window, not 1512](https://github.com/GooeyAI/gooey-server/commit/6e6a45786aa59c5be4bb345b94de0cf19baa9221)
* [Collapse the bar's labels before its controls overlap](https://github.com/GooeyAI/gooey-server/commit/97168b5ea5c5ae682c6db5804e43d5cf1accabbb)
* [Lighten the header rule and give it room](https://github.com/GooeyAI/gooey-server/commit/e9d8617d14d4615b858e9a1ddf98bda32a7724ce)
* [Rule the header, not the whole bar](https://github.com/GooeyAI/gooey-server/commit/35666ad270fbad4d20d7ca405fa51128ced6e132)
* [Stop Duplicate and the publish control sharing one label](https://github.com/GooeyAI/gooey-server/commit/74fb22e97a24dd552d0298b3ffcd7ef60bd51202)
* [Give New Chat and the way back to a published run a home again](https://github.com/GooeyAI/gooey-server/commit/0a7f95cfbbbf3584f09d77320e96bdcaa13cefa1)
* [Do not offer Close Preview where it would leave no tab selected](https://github.com/GooeyAI/gooey-server/commit/09f26c8c64d4b1f9281aac4cbaa461d92a9a628f)
* [The mobile header's wordmark, title width and Ask Gooey mark](https://github.com/GooeyAI/gooey-server/commit/192bac1e0047353bcb09eaad9c6cf24b89e46a40)

## 18-September-2026

**Added**

* [Match the mobile header and tab strip to the Figma flow](https://github.com/GooeyAI/gooey-server/commit/e625a2b27b23aa46be36d5b184840d34751fbc86)

**Fixed**

* [Bound upload metadata filenames](https://github.com/GooeyAI/gooey-server/commit/1be0c076ac96acab7c9fe0b43fa8cfad0927f97f)

## 16-September-2026

**Added**

* [Shimmer loading indicator, fix its SSR readiness race](https://github.com/GooeyAI/gooey-server/commit/ad499e3df8942abc283b0963bcd26f4e1c9d1535)
* [Use previewImg as a blurred loading placeholder for expandable video](https://github.com/GooeyAI/gooey-server/commit/8a978fe0aeec4797a4c14c1b2283402d83263074)

**Fixed**

* [Keep translated raw_tts_text when it matches output_text](https://github.com/GooeyAI/gooey-server/commit/f209b656074d40a02e29ff5703858a2d72c52ba9)
* [Clear stale raw_tts_text between streamed chunks](https://github.com/GooeyAI/gooey-server/commit/d13a18cb7a001fdb7d9a92d472ddb3be9b256380)
* [Letter spacings](https://github.com/GooeyAI/gooey-server/commit/ea4e4aab66d0046ac4012c283620b81cc0c9a3b3)
* [Open About's meta cards in the split, not the editor alone](https://github.com/GooeyAI/gooey-server/commit/1419beed760978bcf6bca179dcd62f43fb8326df)
* [Let a picked view outrank the run reveal, so Usage to Edit lands on Edit](https://github.com/GooeyAI/gooey-server/commit/7394df8fa4b3e5096b9c2da56aeddc45ef2949f3)
* [Underline only on hover](https://github.com/GooeyAI/gooey-server/commit/5f4b3365fdba0977da6ab8c2927c5f622f10ef6f)
* [Keep the view you pick when leaving Usage](https://github.com/GooeyAI/gooey-server/commit/5b4317454cb3261c78a72473804f38b5c642f72c)

## 15-September-2026

**Added**

* [Enable fullscreen preview dialog for generated images](https://github.com/GooeyAI/gooey-server/commit/6e220460abed0fb66a183901d2c77e48bbe44d56)
* [Run metadata in the v2 debug pane](https://github.com/GooeyAI/gooey-server/commit/7ddfb727becef18d9bba03887bdf0e9d538e1ccf)
* [Forward trailing text after extension number to the bot](https://github.com/GooeyAI/gooey-server/commit/2b5dfff4fdf52ad0cf35e778f560d00096e8563d)
* [Give a logged out visitor the browser's own share sheet on About](https://github.com/GooeyAI/gooey-server/commit/1f37b785ea42a8ab2a698fc4015f3b28355d8173)
* [Close the About surface with Privacy, Terms and a Report form](https://github.com/GooeyAI/gooey-server/commit/4c5e2c5420190205c55610d5b9877534c65996f0)
* [Animate the thumbnail-to-lightbox transition with View Transitions](https://github.com/GooeyAI/gooey-server/commit/e80da998fcc1e9cf0d61af21000443795c3f0bac)
* [Run metadata in the v2 debug pane](https://github.com/GooeyAI/gooey-server/commit/d83fdd6a739412e1346696c79c79666c9a08435f)
* [Custom play/pause/mute overlay for inline video, fix dialog action bar overlap](https://github.com/GooeyAI/gooey-server/commit/a96e7ea0e4a9d0cfc2c7b90220e2f6b04dd5cd55)

**Fixed**

* [Two layout regressions and a video-open transition snap](https://github.com/GooeyAI/gooey-server/commit/6f6e83ea87a8845074e482e9ea896dd9d6c4ef99)
* [Sever window.opener before navigating the download fallback window](https://github.com/GooeyAI/gooey-server/commit/1222579de11ca77feabd0c5dfbe98c8a38a4e508)
* [Unique per-instance view-transition-name, reorder helpers](https://github.com/GooeyAI/gooey-server/commit/6dfdc151fbe6c48d62c2f520213b427e2c7bd7c4)
* [Drop the /usage/ endpoint expectation from the v1 layout tests](https://github.com/GooeyAI/gooey-server/commit/d34a3e1d26bf39b16cf0dd266505af86a1d98b94)
* [Flag workflow dialog icon](https://github.com/GooeyAI/gooey-server/commit/300eca762220992b618bfa66cc37f5918f6e8e78)
* [Stop the Debug pane demanding a workspace, which 500'd every public page](https://github.com/GooeyAI/gooey-server/commit/4d8b513cb287c9e3dbddac4fc6cf4c2e49d2b2cf)
* [Give the Builder's panel one key, from one place](https://github.com/GooeyAI/gooey-server/commit/15bb7bd4bde8a71c329710b662e314cc5c6ff842)
* [Read the debug pane's author through current_sr_user](https://github.com/GooeyAI/gooey-server/commit/675d0322886fc91cd0a96ca38a27df67fddd31a9)
* [Stop the Builder closing itself whenever the page it sits beside changes](https://github.com/GooeyAI/gooey-server/commit/a2c04d6cd6706b2e384a4c552849d4299918ea7d)
* [Shrink the Debug pane's type on a phone](https://github.com/GooeyAI/gooey-server/commit/faf0f31803d14b77d2fa2748dc42e10ffb3bc444)
* [Offer the share url wherever there is no dialog, /agent/ included](https://github.com/GooeyAI/gooey-server/commit/416162ae537fe3031605321fde4f36e2449e12ed)
* [Give the page a real h1, and hang the About surface off it](https://github.com/GooeyAI/gooey-server/commit/8f66cb314a243d355fcff6716b881b023c5a4f43)
* [Keep the download fallback within Safari/iOS user activation](https://github.com/GooeyAI/gooey-server/commit/e7b6c29f82a8db26a689296777d68ba114924a16)
* [Move image expand button to top-left, matching video](https://github.com/GooeyAI/gooey-server/commit/867ad5bdb1218d5a556205f88a65e04a8483ad95)
* [Media preview review findings from PR #1097](https://github.com/GooeyAI/gooey-server/commit/54874b10f6112df5d6d49951e1ca73b3b70086c3)
* [Expand button fade grouping and icon direction](https://github.com/GooeyAI/gooey-server/commit/04817f791ed318b72aa02d58a19fbded05fe6af1)

## 14-September-2026

**Added**

* [Add click-to-fullscreen preview for generated images/videos](https://github.com/GooeyAI/gooey-server/commit/83e1090d3d5a41a0fe2d573a18d6f325dd3c5292)

**Fixed**

* [Let the preview dialog backdrop reach the notch/Dynamic Island](https://github.com/GooeyAI/gooey-server/commit/1c641a8efa241ae6b1c5d0f6b83f5ab72aa2fe1d)
* [Suppress Safari's AirPlay icon overlapping the media expand button](https://github.com/GooeyAI/gooey-server/commit/105e20db1eccfc88054bc0252f6eabf468e598fd)
* [Trap and restore keyboard focus in media preview dialog](https://github.com/GooeyAI/gooey-server/commit/57cbde05a73ecbceb9f60818b770a90e9d406748)
* [Prevent media preview expand buttons from submitting the form](https://github.com/GooeyAI/gooey-server/commit/514c6a3a959fbf3109536b59e04ed987b7780b40)
* [Stop a form post counting as arriving somewhere new, and resetting the view](https://github.com/GooeyAI/gooey-server/commit/defb29bbe5ccc8364bf82fd2f9f1e09ec5a8ba9d)

## 11-September-2026

**Added**

* [Enhance chat widget with replay and accurate timestamping features](https://github.com/GooeyAI/gooey-server/commit/0aa1f318fdc3d132f4dfa79c01038e7b01f48087)
* [Enable editing controller-managed chat messages](https://github.com/GooeyAI/gooey-server/commit/3ba52b7269474f92bfc2ec4cbe97f7529b3c016f)
* [Rebuild the v2 mobile chrome on the new screens](https://github.com/GooeyAI/gooey-server/commit/8585e71325373ca4632f9f15dad36b7dc6def1ea)
* [Extend the design system's type to the converted pages, and load it from CSS](https://github.com/GooeyAI/gooey-server/commit/9913d052717ccbbd25d4844e0d022946fe1a4fa9)

**Fixed**

* [Take Share out of the bar's publish control on a view-only page](https://github.com/GooeyAI/gooey-server/commit/e3178fe26b4e6ef1ac643bf9bf60a3bfaa06b515)
* [Stop the mobile crumb repeating the view pill](https://github.com/GooeyAI/gooey-server/commit/17a2a41943800a1b0ccb7549d5bab9dfa5354ef3)
* [Centre the About switcher, and drop the header pill it duplicates](https://github.com/GooeyAI/gooey-server/commit/b8ddf904f7e3662a95056729887d6b3a07a6558d)
* [Move the mobile switcher out of the header, and fix the swap that never fired](https://github.com/GooeyAI/gooey-server/commit/3ca462e57ab2cca9752e91544ccc69946d4d8450)
* [Stop the mobile header showing the switcher twice](https://github.com/GooeyAI/gooey-server/commit/1d630e798c93d0183ef156e6d1542ca1b7724323)
* [Bring the pane slide back, subtler, and stop a run laying out the wrong view first](https://github.com/GooeyAI/gooey-server/commit/59357d91f57ba4bd08c2511e15534ad61e2512a1)
* [Drop the pane slide, which turned every transient layout into a visible round trip](https://github.com/GooeyAI/gooey-server/commit/5d18bb386eba6e8b99ac3537657e5f3bf16d2900)
* [Scope the heading reset to the titles that need it, and give the editor its sizes back](https://github.com/GooeyAI/gooey-server/commit/4687425df0a8977bbc742f1ead4ee67b7d1abd80)
* [Let the About meta heading name only the kinds it holds](https://github.com/GooeyAI/gooey-server/commit/902d66a1cd3cea26879648d03b2c7e75570d5525)
* [Put the Description heading back on About](https://github.com/GooeyAI/gooey-server/commit/5e0c8a2f4fd63a503499c9fcb876fc34de64bb6e)
* [Drop the workflow card title to the design system's UI weight](https://github.com/GooeyAI/gooey-server/commit/3d6f1d9ee24f132c8fe0588d8aa749af6c9ca41d)
* [Reach the bold utilities, and give Ask Gooey's title the display face](https://github.com/GooeyAI/gooey-server/commit/dcd475a99017b539ff443cf4438de80e3f5838c2)
* [Give a card label three lines, and the card one height](https://github.com/GooeyAI/gooey-server/commit/296552f2ced5b1491a21864e36d3d2a373c86a73)
* [Lay the About cards out on a grid, six to a row](https://github.com/GooeyAI/gooey-server/commit/6176e0c5056a7133790680177f6c5c654860482c)
* [Hold the About surface to the design's type and card size](https://github.com/GooeyAI/gooey-server/commit/595d40eea53ce9fd7164751c2f7225fb85f0ff4c)
* [Keep the view a run was started from, instead of imposing the work view](https://github.com/GooeyAI/gooey-server/commit/a94f9a195d8bfc1fe69f5f15ca5652af2716efd8)

## 10-September-2026

**Added**

* [Put the v2 surfaces on the design system's own typefaces](https://github.com/GooeyAI/gooey-server/commit/21a1cf2f17821a67c273fc33879ba52181465a00)

**Fixed**

* [Stop the sidebar forcing the split on every workflow it opens](https://github.com/GooeyAI/gooey-server/commit/cac0ae08bd21ea1df7d4091b27bcc15fb3cda2e0)
* [Settle three details of the v2 chrome](https://github.com/GooeyAI/gooey-server/commit/8c3158da4d9a84f8f1d36edd58276a7dab35c846)
* [Keep the page-load bar out of the app talking to itself](https://github.com/GooeyAI/gooey-server/commit/8649234dc70c018e45c51fc41180bbf7271b7e2b)
* [Take the v2 workspace's width off Bootstrap's container](https://github.com/GooeyAI/gooey-server/commit/04deb60d1f865b34f718834bf7aaca4e286eafcb)
* [Open a published run on About, a saved run on the work view, and drop the editor's dotted ring](https://github.com/GooeyAI/gooey-server/commit/e2bfc238a1ae3d4a1969698635d41cf5ff32809c)
* [Let the instruction editor own its scroll, and open every workspace on About](https://github.com/GooeyAI/gooey-server/commit/5a6bee055adaa5841010d71b881ba5ad8ce567df)
* [Correct the top bar's gates on a root recipe and a view-only page](https://github.com/GooeyAI/gooey-server/commit/1134b80da1c80434f352a78c573d836c317b78de)
* [Give layout v2 a heading outline a crawler can read](https://github.com/GooeyAI/gooey-server/commit/75fc91765b4aad9aca8cc769f627b4509b53ac6c)
* [Upgrade Azure Speech SDK for CRL compatibility](https://github.com/GooeyAI/gooey-server/commit/8403e9ad495cd98245008cfa0fdad5cd066a933d)

## 09-September-2026

**Added**

* [Turn on showRunTime for /agent and the builder](https://github.com/GooeyAI/gooey-server/commit/05e156db825c4a07e4c25fd2f6c3344dfab1fd30)
* [Add GPT Image Sunburst and Flare](https://github.com/GooeyAI/gooey-server/commit/8e45aedc3e769379f4a7b732392517c0f846f60f)

**Fixed**

* [Renumber image generation migrations for master](https://github.com/GooeyAI/gooey-server/commit/969af49ac3ef53426283a9ac03bd685ebc451422)
* [Ignore avoid repetition for all runs](https://github.com/GooeyAI/gooey-server/commit/346a26908544f79b1621e2e4f26f2c54cff42572)
* [Send the Examples tab to explore from a published run too](https://github.com/GooeyAI/gooey-server/commit/4202b6f7adc958d8f2c0ffccfcbe463ca3545092)
* [Keep a shared example link pointing at the run it named](https://github.com/GooeyAI/gooey-server/commit/2bf17b7532e867e879478044b4dd4f8e85a3c2f5)
* [Let a keyboard close the top bar's menus, and stop the shell re-rendering everything](https://github.com/GooeyAI/gooey-server/commit/03f90f030e1698ed2676580a921f5b29afda7b8d)
* [Correct GPT Image 2.5 token pricing](https://github.com/GooeyAI/gooey-server/commit/9878a226741f9cfd4d9d46bc7ad689bdea4bda23)
* [Use GPT Image 2.5 model identifiers and labels](https://github.com/GooeyAI/gooey-server/commit/6f19eb370b4774cb64f0c48791ac78f4a5e43892)

## 08-September-2026

**Added**

* [Quote the interrupting message when a streamed WhatsApp reply is replaced](https://github.com/GooeyAI/gooey-server/commit/95fec8e91b9adee06e7929d34400355b79b41580)

## 07-September-2026

**Fixed**

* [Authorize builder runs before submission](https://github.com/GooeyAI/gooey-server/commit/28505d0530f79b5822ead854cf059bf959c32b6e)

## 06-September-2026

**Added**

* [Stream Fireworks chat completions](https://github.com/GooeyAI/gooey-server/commit/841fd5f76151128aa695ac54398d06edbfba7a75)

## 04-September-2026

**Added**

* [Add run time in the assistant message](https://github.com/GooeyAI/gooey-server/commit/8fff223b4175b78ed32229970a7324b94e79fc20)
* [Report how long the answer took on the response message](https://github.com/GooeyAI/gooey-server/commit/6d24c8292f1f0693565ba15da8d304d3a4d390f4)
* [Add RunTimeline component and integrate debug pane refactor](https://github.com/GooeyAI/gooey-server/commit/91e4c586371ff6a6be64636dd1945863de213bfd)
* [Open layout v2 to everyone, scoped to the recipes forked to it](https://github.com/GooeyAI/gooey-server/commit/41276e5a3c2af4349e07e1e674767ef1867bb05b)
* [Name a workflow's run count in About, not its owner's output](https://github.com/GooeyAI/gooey-server/commit/b28debb363238b4673e4ed9f607e8f5c3f3f71e5)

**Fixed**

* [Send created_at in the assistant entry too](https://github.com/GooeyAI/gooey-server/commit/5135ede30a8b89f08d78d339d6cd1fcd034b621f)
* [Avoid duplicate agent knowledge controls](https://github.com/GooeyAI/gooey-server/commit/f9d2c6e264e457ce18a41d1800389019891d8afb)
* [Scope agent pane tab styles](https://github.com/GooeyAI/gooey-server/commit/3a93428eca0261715cb4853bb3879ba20615e189)
* [Polish new-page suggestions](https://github.com/GooeyAI/gooey-server/commit/36868bbad3b041c0320adc1774b08d6dddb97a9b)
* [Relativize the rail's Ask Gooey href before navigating](https://github.com/GooeyAI/gooey-server/commit/cc81ada4050e3324dcfcab0018033f3cf1096288)
* [Only leave the editor for the split when a run starts](https://github.com/GooeyAI/gooey-server/commit/7873f17f57dd261b571677635fc030d81c4ab4c7)

## 03-September-2026

**Added**

* [Give the mobile sheet a menu per state](https://github.com/GooeyAI/gooey-server/commit/a962f800ede29ee090809e47ef4dd1521573039f)

**Fixed**

* [Stop the insufficient-credits card from scrolling](https://github.com/GooeyAI/gooey-server/commit/1e98d8294af87706aec6334f4f4a620caf8956d0)
* [Rerun insufficient-credit workflows in fallback workspace](https://github.com/GooeyAI/gooey-server/commit/2b0bc2dc3a370390063aae30eb49763036200ef7)
* [Preserve partial reply display content](https://github.com/GooeyAI/gooey-server/commit/52d73d9a9ddc21ab6e5f0ec8d1eaf111f77e2431)
* [Switch agent panes without refetching](https://github.com/GooeyAI/gooey-server/commit/a8cb01050ca972a4094a74abf6d9087c78e55fe6)
* [Keep the Builder panel off the tabs with no workspace](https://github.com/GooeyAI/gooey-server/commit/5f713c073d457bd8521958abf8cea1352814d3c0)
* [Put Update back in the Usage tab's bar](https://github.com/GooeyAI/gooey-server/commit/8a8a24f8e92fd7fa7ce33d2fedc16013c3ec1481)
* [Keep Run and Update out of the Usage tab's bar](https://github.com/GooeyAI/gooey-server/commit/b38198cba97e66ccc8cbd04c7b230277d3925f0c)
* [Send a v2 recipe's Examples tab to the explore gallery](https://github.com/GooeyAI/gooey-server/commit/724a32e726ad6b3c38e1f035221ee93e3fe3acb5)
* [Anonymous user runs should be saved but not started until after login](https://github.com/GooeyAI/gooey-server/commit/a0aa7a00115163dd885cc694f568b156cf0f4b71)

## 01-September-2026

**Fixed**

* [Handle insufficient credits in builder](https://github.com/GooeyAI/gooey-server/commit/95b849910b01c93481d0609ec57ff22859d60f69)
* [Avoid freezing admin on large JSON fields](https://github.com/GooeyAI/gooey-server/commit/7d5775e1cfbd7b4fcd92a69b1b1be055c016e089)
* [About margins](https://github.com/GooeyAI/gooey-server/commit/2fcd5a76ebd61af5027824d87fc16fb90438f5b4)

## 31-August-2026

**Added**

* [Give About an owner, its tags, and one panel to hold them](https://github.com/GooeyAI/gooey-server/commit/1c5a4c085c56b3dd0bafb59aea2f510c82437ca0)

**Fixed**

* [About cards alignments](https://github.com/GooeyAI/gooey-server/commit/bb2310abded9f94b228e4a90f214850e68abbc22)
* [Remove addtitional padding](https://github.com/GooeyAI/gooey-server/commit/65a32aa8b0c7b0ad801a1aed0ee7dda58bec9ac2)
* [Make About readable on a phone](https://github.com/GooeyAI/gooey-server/commit/cec022fcc6f9628554a5ea5fbe10ab444451edf8)
* [Read the tab set from edit permission, not authorship](https://github.com/GooeyAI/gooey-server/commit/0b713bf01d2690f8bf87b13efbc4d26967ce0aa0)

## 30-August-2026

**Fixed**

* [Make saved run surface editable in admin](https://github.com/GooeyAI/gooey-server/commit/11f5e946b01eb86b281995aba469d909717673f7)
* [Fix the layout v2 tests](https://github.com/GooeyAI/gooey-server/commit/fd6237b5496fe6c6c6614b42b327668565bd26bb)
* [Duplicate run bars!](https://github.com/GooeyAI/gooey-server/commit/65c4368a1c90cab2a25c2da7c432590008cf66e8)
* [Correct font size](https://github.com/GooeyAI/gooey-server/commit/58d4cdcb0c30d17e653de63510ecb21e52bac898)
* [Keep the mobile nav drawer open while a run streams](https://github.com/GooeyAI/gooey-server/commit/0372382749aaceb9575f10ffca441029a2396974)
* [Move the editor's run bar into the editor pane](https://github.com/GooeyAI/gooey-server/commit/5e1bd27b65bde7a6822756b6072160d3214f2547)
* [Point the sidebar's API link at the workspace's own keys](https://github.com/GooeyAI/gooey-server/commit/e561085e08773bc3742d80336fc8f1b13afee5d8)

## 29-August-2026

**Added**

* [Enable layout v2 by default](https://github.com/GooeyAI/gooey-server/commit/64170ec2a1f2c67b0e28b3c8769fe33c6e35a660)

**Fixed**

* [Underline recipe title link](https://github.com/GooeyAI/gooey-server/commit/f44d2f337286ade20749da463d0fe1330c4c052a)
* [About deployements cards link](https://github.com/GooeyAI/gooey-server/commit/b9f48670acf2464f40edce47fd2e13806730bf62)
* [Layout v2 mobile navigation and view defaults](https://github.com/GooeyAI/gooey-server/commit/7f43fe6524db6673fa8a8d63b06d9ddd0eb878c0)
* [Correct formatting](https://github.com/GooeyAI/gooey-server/commit/3c079ac1b68bff8c3c1fe025f8aade9216a5b083)

## 28-August-2026

**Added**

* [History page and per-app Usage tab](https://github.com/GooeyAI/gooey-server/commit/3b9c807376f0971a24706f548b59703c9ba36a1b)

**Fixed**

* [Strip thinking traces for non WEB deployments](https://github.com/GooeyAI/gooey-server/commit/21d621b676e5808dc9c1b36818dcadf1787634d7)

## 27-August-2026

**Added**

* [Title menu with version history, duplicate and delete](https://github.com/GooeyAI/gooey-server/commit/b38faf34209a144059824c567b7ed4375becc634)

**Fixed**

* [Keep top bar actions available during requests](https://github.com/GooeyAI/gooey-server/commit/9e34c776b580e94528e22ecff941f99a3bc16e32)
* [Suppress regenerate for agent workspace](https://github.com/GooeyAI/gooey-server/commit/0dfec120af14121f22c000e008ce007d5f898084)
* [Preserve workspace pane scroll ownership](https://github.com/GooeyAI/gooey-server/commit/723d00480ac45a50fdb9fdfca646e29ead4018fe)
* [Preserve builder state across layouts](https://github.com/GooeyAI/gooey-server/commit/31775fc2a5ea87ef955d04348391d796f680e3a5)
* [Keep layout v2 execution on legacy page](https://github.com/GooeyAI/gooey-server/commit/48bae6c1eaadcbe69d1df12fc6b237abb69b4d8c)
* [Styling tighness](https://github.com/GooeyAI/gooey-server/commit/22f6daf8be2b8e8896c940baa28bc7f3113d6548)
* [Close an unterminated css comment](https://github.com/GooeyAI/gooey-server/commit/e0f764d074bcc765847100fbccd386a73a607321)
* [Stop a notice above the chat preview clipping the bottom of it](https://github.com/GooeyAI/gooey-server/commit/17ad54bbd5e000a31fac5ed668cce562002f54ff)
* [Give the top bar's controls one height](https://github.com/GooeyAI/gooey-server/commit/daf5ddcfe40f4a9cce2f03e2ab380a9314b5c881)

## 26-August-2026

**Fixed**

* [Persist a superseded WhatsApp run's partial reply](https://github.com/GooeyAI/gooey-server/commit/8b9b504f0ea17c461869a5167c02793a32c24b89)
* [Coordinate WhatsApp event batching on a row lock](https://github.com/GooeyAI/gooey-server/commit/36957b2f6507a928079e548368c6359061c79045)
* [Stop the narrow-viewport fold eating the layout the user picked](https://github.com/GooeyAI/gooey-server/commit/9ed28f582b23842837c949c27d135b11c672a599)

## 23-August-2026

**Added**

* [Use GPT Transcribe as default ASR](https://github.com/GooeyAI/gooey-server/commit/d579e9f6f370afc1b094034a4d7bd9ffa1133737)
* [Add GPT Transcribe ASR model](https://github.com/GooeyAI/gooey-server/commit/26c1f796119cc6c20a85e823cc04822e7362ff8f)

**Fixed**

* [Retry transient Chirp operation polling failures](https://github.com/GooeyAI/gooey-server/commit/89bd1e3b4d6d38286ca825fe2dabf9429249fd95)

## 22-August-2026

**Added**

* [Add Google Chirp 3 ASR](https://github.com/GooeyAI/gooey-server/commit/34214ef858e7b4b4f82ec297bbe75c605e5d75ab)

## 20-August-2026

**Added**

* [One mobile header, and Ask Gooey as the root of the stack](https://github.com/GooeyAI/gooey-server/commit/8c8d8e983de54389b84d3d5ae0197ecb359e35d0)

**Fixed**

* [Fix usability bugs](https://github.com/GooeyAI/gooey-server/commit/94e36ddc5f3a20683601158fb7f1efbc336221e3)
* [Bottom padding for modal](https://github.com/GooeyAI/gooey-server/commit/ed9b69da1cc41452c0e276f8aa0b36ccf77e0986)
* [Bound the v2 shell at every width, and let the Builder announce its own state](https://github.com/GooeyAI/gooey-server/commit/697f2aec6f86a43f32401c171258c242a0e7419f)
* [Shorten placeholder](https://github.com/GooeyAI/gooey-server/commit/ab6a6d9306cdd25e8579ad56535ee7d43f8d9443)
* [Stop the mobile drawer scrim from staining Safari's edge strips](https://github.com/GooeyAI/gooey-server/commit/104dc5dc60f20e60bd58814049221f0120f17462)
* [Avoid zoom on focus for mobile devices](https://github.com/GooeyAI/gooey-server/commit/1b3316a75adedf6cabba08f11a0500b7b03b8cfd)

## 19-August-2026

**Added**

* [Allow credit topups for personal workspaces](https://github.com/GooeyAI/gooey-server/commit/cecfd1af861737bec68096f085974db90c64b2c6)

**Fixed**

* [Close the mobile nav drawer on navigation](https://github.com/GooeyAI/gooey-server/commit/70a0db9e6babd1030ba78791a259ea87492a7e8f)
* [Reduce control sizes](https://github.com/GooeyAI/gooey-server/commit/06c6f3001ec9831b11a560fe7efc15137829e56b)
## 17-August-2026

**Fixed**

* [Use a plain logout link](https://github.com/GooeyAI/gooey-server/commit/84a7dd8a17a276dffffd8c39aec696de12279602)

## 16-August-2026

**Fixed**

* [Harden SraVaani Modal inference](https://github.com/GooeyAI/gooey-server/commit/0a3190f0c8a0ea10e867c9d2f12f78620c8d5c96)

## 12-August-2026

**Fixed**

* [Keep LiteLLM initialization provider-scoped](https://github.com/GooeyAI/gooey-server/commit/b194a37c3531e9dff99091602b8aeab70e6fdf61)
* [Gate document intelligence providers](https://github.com/GooeyAI/gooey-server/commit/1f722afb9d69e259c40bd880272a441c55843964)

## 11-August-2026

**Fixed**

* [Stop the chat preview showing an empty assistant bubble](https://github.com/GooeyAI/gooey-server/commit/5eac2d9008f2f61beb9f6034abf9f1237dbce11d)

## 10-August-2026

**Added**

* [Use builder and whatsapp themes](https://github.com/GooeyAI/gooey-server/commit/0c4bb2b2eacb9476a7ed43389676cd5deaed926a)

**Fixed**

* [Exclude Outlook from verified email credits](https://github.com/GooeyAI/gooey-server/commit/fc2cdfdea574308d1fd2e0c993a04b83ecd58c0c)

## 08-August-2026

**Fixed**

* [Align chat widget history tests](https://github.com/GooeyAI/gooey-server/commit/7f5086543569abc54729e366cc9d7733d8b861b0)

## 07-August-2026

**Added**

* [Preserve input documents / audio / images on chat window](https://github.com/GooeyAI/gooey-server/commit/bb3a36617b1e7b73d0f2af757c08b31d9591583f)
* [Carry run metadata on chat history messages for widget export](https://github.com/GooeyAI/gooey-server/commit/3d5c13cf193f5031b4591b30781d6fc71ba553ba)

**Fixed**

* [Preserve gemini thought signature](https://github.com/GooeyAI/gooey-server/commit/640243bfb07de47ae0ebc2cd6fc3b7d04b748eea)

## 05-August-2026

**Added**

* [Add `to_llm_body` utility for message field validation and refactor message handling](https://github.com/GooeyAI/gooey-server/commit/69de9b0ae0f6d9d5752d5890b0e93c58fdd26d80)
* [Add New item to navigation sidebar](https://github.com/GooeyAI/gooey-server/commit/ac505339772afb382b1ad4528194c602d7c1634b)

**Fixed**

* [Make message threads searchable in admin](https://github.com/GooeyAI/gooey-server/commit/2d60155d9ffa985f46f5eca705d9b98d944e1ac2)
* [Add support for `additional_properties` in workflow tools and LLM tool definitions](https://github.com/GooeyAI/gooey-server/commit/e55d46b5cbf1376f0cbea06bbb5c130c22d6606a)
* [Add `message_thread` to autocomplete fields in admin panel](https://github.com/GooeyAI/gooey-server/commit/7783222c5d9ea4dfe0aee8843cb94a8fe2a309a4)
* [Improve workflow state serialization in update workflow tool](https://github.com/GooeyAI/gooey-server/commit/ff059f44da659d7f67ea8354d6f6caa4997cad28)
* [Update redirection logic in `bind` to handle builder prompt surface explicitly](https://github.com/GooeyAI/gooey-server/commit/df33142e5c13dce5dba7e786507f01f48815a2f5)
* [Centralize login redirection logic with `get_login_url` across routers](https://github.com/GooeyAI/gooey-server/commit/da2fe92730e293f092d92272d73c719ad76b8c3e)
* [Redirect unauthenticated users to login on AskGooeyNew page access](https://github.com/GooeyAI/gooey-server/commit/25e3be4a1f10743d36d815aca9899dbb5e5cdf32)
* [Preserve single Bulk Eval metric labels](https://github.com/GooeyAI/gooey-server/commit/604888fd00db4e4b5c3a45b2e24063a92a826daf)
* [Home landing page links](https://github.com/GooeyAI/gooey-server/commit/9453c03e8d6892981f17df7a16dcfb524356bc37)
* [Show standalone builder conversations in the navigation sidebar](https://github.com/GooeyAI/gooey-server/commit/9921ddafb4072f5cf17b9eb5bf41171af38c8dd9)
* [Invalidate workspace cache once per sidebar render](https://github.com/GooeyAI/gooey-server/commit/d2b93163b799a67f2f85238b2acb8d488e2ab82c)
* [Address PR 1040 review comments](https://github.com/GooeyAI/gooey-server/commit/0afb68b1755400af09d8ee04beb564a8695ffae3)
* [Ask Gooey full-width + responsive layout](https://github.com/GooeyAI/gooey-server/commit/7988264bb9839bf018172d13605cf429f3087a3f)
* [Remove footer for now](https://github.com/GooeyAI/gooey-server/commit/efa768453edfe2e2d35ea2ff2200dc502b846eec)
* [Skip missing Bulk Eval aggregations](https://github.com/GooeyAI/gooey-server/commit/138dcba5c97860c2954d61499077c701dacb9495)

## 04-August-2026

**Added**

* [Integrate live transcription into AskGooeyNew with mic UI and backend API support](https://github.com/GooeyAI/gooey-server/commit/9990d936113daffee0e265f86ed5c7da851fdb70)
* [Add file attachment support to AskGooeyNew with upload handling](https://github.com/GooeyAI/gooey-server/commit/fdf105d6dfb1d9e1a09df363cef544b3126abd1a)
* [Update AskGooeyNew UI with contextual placeholder, refined styles, and scrollable suggestions](https://github.com/GooeyAI/gooey-server/commit/6b6e82d73216dc4a9356d923ec6b79051f0d3cc1)
* [Add /new/title-run\_id to render standalone ask gooey without associated workflow](https://github.com/GooeyAI/gooey-server/commit/d51f4fd3ef767a03b4023ab97dfa5ca4170ddea4)
* [Add Sarvam speech generation and recognition](https://github.com/GooeyAI/gooey-server/commit/71fa241c728c0fc0c8b2083abf2cb53cde5ab3d5)

**Fixed**

* [Update AskGooeyNew text color logic based on input presence](https://github.com/GooeyAI/gooey-server/commit/bb31898acddd85d3a7979c8536de3b66fa5275e2)
* [Support explicit Bulk Eval skips](https://github.com/GooeyAI/gooey-server/commit/e14fae344a079e2ea0f46fed005bbeb94b34520f)
* [Resolve Bulk Eval models before evaluation jobs](https://github.com/GooeyAI/gooey-server/commit/5c51b2d25e734add9d89062e735c5a5399b9659c)
* [Chunk Mayura translation inputs](https://github.com/GooeyAI/gooey-server/commit/dc8a55acfabe1db68af4550025ef48774e037ff3)
* [Validate Sarvam TTS audio response](https://github.com/GooeyAI/gooey-server/commit/a095799e031c013ea18124c5281e609efce929d4)
* [Address navigation sidebar review feedback](https://github.com/GooeyAI/gooey-server/commit/dd82a3b5fa76d9fad53c6036e4fa9da021c6f9ab)



## 03-August-2026

**Added**

* [Add Sarvam Mayura translation](https://github.com/GooeyAI/gooey-server/commit/267b8aa866615055a0e9d58306ca91a6d6fd173d)

## 01-August-2026

**Added**

* [Add UpdateConversationTitle tool and integrate it into Gooey.AI (#1042)](https://github.com/GooeyAI/gooey-server/commit/6319896ad004eb5af98bb1eebda4e0f5583e7d26)

## 31-July-2026

**Fixed**

* [Let Bulk Eval judges correct invalid tool calls](https://github.com/GooeyAI/gooey-server/commit/ae398205252d51764a5c3b8a62d9888b7e902021)

## 30-July-2026

**Fixed**

* [Handle missing Azure moderation endpoint in `is_image_nsfw` gracefully](https://github.com/GooeyAI/gooey-server/commit/3a82575120e9e17aa812df090e68391c95cb6df0)

## 28-July-2026

**Added**

* [Add LiteLLM Responses provider](https://github.com/GooeyAI/gooey-server/commit/9a980b0212dc54553730409324341ffde9df628f)

## 27-July-2026

**Fixed**

* [Avoid Modal initialization for TTS language options](https://github.com/GooeyAI/gooey-server/commit/c75def3a9d9c02334b5137a5200df216a96c9087)

## 24-July-2026&#x20;

**Added**

* [Optimize conversation fetching by limiting fields retrieved](https://github.com/GooeyAI/gooey-server/commit/b61ceba6342a6b97c5dfe9378e5125aad686b0b5)

**Fixed**

* [Check message thread ownership via first\_run/last\_run to avoid slow query](https://github.com/GooeyAI/gooey-server/commit/0f707de10c274825a7c23b27af18612baa7ba54a)

## 22-July-2026&#x20;

**Added**

* [Convert MessageThread's last\_run to OneToOneField, filter by latest run in listings](https://github.com/GooeyAI/gooey-server/commit/721246766e7720aa9385b77e07ee5f41a22aa5bb)

## 21-July-2026&#x20;

**Added**

* [Enhance MessageThread admin display and refine thread selection logic](https://github.com/GooeyAI/gooey-server/commit/2d433f2cd7941ec3b2f5252444b75abc36aae7fc)
* [Re-add MessageThread migration after correcting dependency](https://github.com/GooeyAI/gooey-server/commit/c2b2fdd30b870268d530bb1ea97776249d72086e)

**Fixed**

* [Fix Silk duplicate key](https://github.com/GooeyAI/gooey-server/commit/9a659309268058dc9534504d57e20ea3eb10f852)

## 20-July-2026&#x20;

**Added**

* [Record MessageThread from agent saved runs](https://github.com/GooeyAI/gooey-server/commit/a217572b9356dc1a3e700fb2bf404bafb4b45001)

**Removed**

* [Revert "support multi-select tag filters"](https://github.com/GooeyAI/gooey-server/commit/56a729c8215df2314d683b8779a7c0c03fd0fcc7)
* [Revert "show tag filters with text search"](https://github.com/GooeyAI/gooey-server/commit/d7581e8836a13a43ce511fd57ff79c553b0c4ac8)

## 18-July-2026&#x20;

**Added**

* [Make `run_id` unique in `saved_run` model](https://github.com/GooeyAI/gooey-server/commit/973610d8afa3ddf033922d0293d5f4cc8547d087)

## 17-July-2026&#x20;

**Added**

* [Support multi-select tag filters](https://github.com/GooeyAI/gooey-server/commit/2a1d3314b0eb57ced387951f49c787b0865ef3af)

**Fixed**

* [Fix spacing and pill borders](https://github.com/GooeyAI/gooey-server/commit/cada356526b7a7a562665dd45c170c2b7a82da58)
* [Show tag filters with text search](https://github.com/GooeyAI/gooey-server/commit/dd754701e0c88c6198e0dc52e563433d9c2d2543)

## 16-July-2026&#x20;

**Added**

* [Add tag filter to explore search](https://github.com/GooeyAI/gooey-server/commit/65c9cd79a29f0373dd18e5f9e78ea2cee130d188)

## 14-July-2026&#x20;

**Added**

* [New /history page](https://github.com/GooeyAI/gooey-server/commit/6f542694d6f7041d54eaac436ff9832b575ded7f)

## 13-July-2026&#x20;

**Fixed**

* [Refresh dynamic tools in reused Realtime sessions](https://github.com/GooeyAI/gooey-server/commit/7ba6c47ad9cac5558cdf18511d8e0cd4c6b58e58)

## 09-July-2026&#x20;

**Added**

* [Replace Deno with Cloudflare Workers](https://github.com/GooeyAI/gooey-server/commit/625003c0b360f5bdf43c60d28a9cdc98ac76f659)

## 07-July-2026&#x20;

**Fixed**

* [Fix analysis page showing 404 without access](https://github.com/GooeyAI/gooey-server/commit/7bbebce142536562d14d4bbc442704e933bc130b)

## 01-July-2026&#x20;

**Fixed**

* [Fix db\_middleware overriding endpoint signature and breaking FastAPI](https://github.com/GooeyAI/gooey-server/commit/c1705f835070e633d9e8d546559eb27a8414bf90)
* [Handle blank WhatsApp body text](https://github.com/GooeyAI/gooey-server/commit/ec3815de90c5e4db62bb2c92e0eabb0b0f424682)

## 25-June-2026

Added

* [New /account/memory view to browse saved memory entries](https://github.com/GooeyAI/gooey-server/commit/4b39f90e905ac3df34db9b16b31b0b6a63ba52f6)
* [Filters for the /account/memory view](https://github.com/GooeyAI/gooey-server/commit/4466146a2201330438fa8538382d0ccc2c4d6f1c)
* [Scope and relationship fields added to MemoryEntry model](https://github.com/GooeyAI/gooey-server/commit/4e881b2645a0cf3ad14e45bb56077c56dddea9c7)
* [Language-based filtering for TTS providers and voices](https://github.com/GooeyAI/gooey-server/commit/7749ba73426dad24927438e7be4b20a655f025bb)

Fixed

* [Correct button alignment in list view editor](https://github.com/GooeyAI/gooey-server/commit/c102612532acf45cc79356a35d0871d921b1f3d9)
* [Fix TTS/ASR filter selector key in VideoBots](https://github.com/GooeyAI/gooey-server/commit/3c335279863edd447d7920b5bd5674b5ebeaa872)
* [Guard Google TTS language lookup when credentials are missing](https://github.com/GooeyAI/gooey-server/commit/195ceacca0b15db22fa1fcd60661051a651f19cb)
* [Refresh stale Google TTS voice cache after shape change](https://github.com/GooeyAI/gooey-server/commit/837e7cc1f147b1c42094c2bea62e8cd67001cbc6)
* [Update language filter label for clarity](https://github.com/GooeyAI/gooey-server/commit/349ac37bf65288a3b4f67069669a763468da9899)
* [Fix home saved card — clamp description and cap thumbnail height](https://github.com/GooeyAI/gooey-server/commit/1270fb0d844e024729861c0d8a5b87720b84d4a9)

## 23-June-2026

Fixed

* [Healthcheck fix](https://github.com/GooeyAI/gooey-server/commit/2f17ad52b06c8ac6a2d33b67fb49d5b27d5a885d)
* [Fix Composio meta tools running in an in-process tool-router session](https://github.com/GooeyAI/gooey-server/commit/8ad2e4c1eea320f5d24e8e2e397aee98cf942dd5)

## 22-June-2026

Added

* [New /home page launched for logged-in users](https://github.com/GooeyAI/gooey-server/commit/ebbe88c7c5982871473fe2701b221f74e6dbe900)

## 19-June-2026

Fixed

* [Truncate long workflow card titles in history view](https://github.com/GooeyAI/gooey-server/commit/7af9e62c0aa2a521f74203fa549ea76acc07aed0)
* [Show Home page link in mobile menu](https://github.com/GooeyAI/gooey-server/commit/6479d90c67f5cc2f85c43ae8bd848fc900238c23)
* [Allow workflow tab selector to scroll](https://github.com/GooeyAI/gooey-server/commit/1443ee40e3c4d6df88c19d4ee5a0c699a3d2a50a)
* [Fix text clamping and mobile grid layout for recent workflows](https://github.com/GooeyAI/gooey-server/commit/27e7d3a7bdf1901170441f9f6c07aeae91a5b1ba)

## 18-June-2026

Fixed

* [Correctly save run transaction and price data](https://github.com/GooeyAI/gooey-server/commit/8de9bd55b91fc0240c6d20cb0ae8eedc22f11bd8)
* [Show all workflows in Gooey Builder conversations](https://github.com/GooeyAI/gooey-server/commit/7b7d76d86d2c2b72aadbda2616d4d278fa8d759e)
* [Persist run price correctly in SavedRun and clean up bulk progress UI](https://github.com/GooeyAI/gooey-server/commit/80674ddc881936d3d5a7419020366ccf46bcf66b)
* [Map cancelled bulk runs to stopped state after completion](https://github.com/GooeyAI/gooey-server/commit/76add6c1614974d51effc6d404b7916e57803052)
* [Report correct starting row number in bulk progress display](https://github.com/GooeyAI/gooey-server/commit/4a422221e720967da6afcf8e0d339534d976e08a)

## 16-June-2026

Added

* [Support for local file storage](https://github.com/GooeyAI/gooey-server/commit/83f29e42ddde12da30f4650de338f975ca026948)

Fixed

* [Fix local file uploads from the web widget](https://github.com/GooeyAI/gooey-server/commit/bb79fbbef9295d93da0406e6c0f254fdea31c2fe)

## 13-June-2026

Added

* [Track call site with a new surface field on SavedRun; filter history and builder conversations by surface](https://github.com/GooeyAI/gooey-server/commit/4cd6c24dccd6a7330a725e710a6e7ccc45f5a28a)

Fixed

* [Scope OpenAI TTS voice options to the selected model (adds Marin & Cedar voices)](https://github.com/GooeyAI/gooey-server/commit/90ae57966d154d825fde7adc9544cae7cad86ff1)
* [Migrate OpenAI Realtime WebSocket to GA interface](https://github.com/GooeyAI/gooey-server/commit/d61ce0f8287ca411fb575515adbd69f02fb5f500)
* [Remove temperature from OpenAI Realtime audio path](https://github.com/GooeyAI/gooey-server/commit/1a1e0d7a90752c5f594cf5929d36851989630a33)

## 10-June-2026

Added

* [Bulk runner progress display](https://github.com/GooeyAI/gooey-server/commit/07db9669b27e99f6b2b76688222704fdb121d570)
* [Reordered bulk run complete stats and added per-workflow elapsed timer](https://github.com/GooeyAI/gooey-server/commit/9ef0e40d002ab2181d341da24fe33af8ebcbc940)
* [Font Awesome icon and color support for Tags on the home page](https://github.com/GooeyAI/gooey-server/commit/18fd207deb027c9e0e92bd63694be212404371a9)
* [Font Awesome icon and color support for WorkflowMetadata; wired to home page icons](https://github.com/GooeyAI/gooey-server/commit/4bf9778904b71f38af98986b64fa1d38d4bbaf1f)
* [Link CMS workflow tabs to WorkflowMetadata](https://github.com/GooeyAI/gooey-server/commit/d09bee9038bbc558c554f25d8b4412b85ebd418e)

## 07-June-2026

Fixed

* [Improve Composio error handling](https://github.com/GooeyAI/gooey-server/commit/a83fcaf9d07bfbb0d320fa5d1ea2cb7556304a1d)

## 05-June-2026

Fixed

* [Hide Gooey Builder runs from non-admin users](https://github.com/GooeyAI/gooey-server/commit/20817d665e8dfec6333648ac0ce5e0b13f617fbc)
* [Restore real-time updates from both workflow and builder channels](https://github.com/GooeyAI/gooey-server/commit/42215fd02177a13e49aaace9889a00ed2d7d1697)
* [Fix document JSON parsing](https://github.com/GooeyAI/gooey-server/commit/40a2fefc7493a10c29d9c81c897329d6d482b403)
* [Restore error metadata so custom error widgets render correctly](https://github.com/GooeyAI/gooey-server/commit/4a5b10352d272b0e98db256851aa5f39ccf18023)

## 02-June-2026

Added

* [Close dialogs by pressing the Esc key](https://github.com/GooeyAI/gooey-server/commit/989ef6b0b107fd738cdacf526cef8654dc2a1b7f)

## 29-May-2026

Fixed

* [Prevent stale Bulk Eval columns from producing phantom evaluation results](https://github.com/GooeyAI/gooey-server/commit/f174d8eb81be2f963c361f918db99ff95b77c215)
* [Align workflow URL action buttons correctly](https://github.com/GooeyAI/gooey-server/commit/9b2e287131f85dec763a8c437ea33d409aa7d0fb)

## 28-May-2026

Fixed

* [Improve error handling in workflows](https://github.com/GooeyAI/gooey-server/commit/c76941232916862a78b38a7598311d32a08131fc)

## 26-May-2026

Fixed

* [Show API runs only under History → "All", not under "Just me"](https://github.com/GooeyAI/gooey-server/commit/e065b170f0c67dbffa73eacfd24f83be76727b3e)

## 19-May-2026

Added

* [Support for Fal billable units and improved pricing handling](https://github.com/GooeyAI/gooey-server/commit/db0c37d5937cf1870194e9584295c4654cfe1e96)

Fixed

* [Ensure pricing is correctly saved after model changes](https://github.com/GooeyAI/gooey-server/commit/51497e3978242d9a2747aaa720cfc60c008ced3d)

## 15-May-2026

Added

* [Pagination on the workflow search page](https://github.com/GooeyAI/gooey-server/commit/5e455911c41600e7857faedf58046995008cfd4c)
* [A7, A30, R7, R30 retention columns in messages CSV export](https://github.com/GooeyAI/gooey-server/commit/17bdbabc71a0ba71e19023ec1c2b092380b63db0)

Fixed

* [Resolve infinite redirect loop on invalid pagination cursor](https://github.com/GooeyAI/gooey-server/commit/db3bd49883547eb362e3ab9726823d32d546a6e9)
* [Redirect to first page when pagination URL is malformed](https://github.com/GooeyAI/gooey-server/commit/ac8bdcd163d0d0b1b462f2f9f6f62fd6293a06bf)
* [Handle invalid URL parameters for pagination gracefully](https://github.com/GooeyAI/gooey-server/commit/96e906ff3d08eb0b2ebb804521468d316b006f62)
* [Prioritise the user's own workflows in the featured list](https://github.com/GooeyAI/gooey-server/commit/a73427fa30885b94b1352bf283ca0dfe280c83bc)
* [Show detailed feedback toggle in admin panel](https://github.com/GooeyAI/gooey-server/commit/5937ad8562282d2032c6da6dd9eaa5a9ef6eb0a2)
* [Allow the detailed feedback toggle to be changed independently](https://github.com/GooeyAI/gooey-server/commit/f2cb98e3a177f1e61623ae9fa245e162f25a9496)
* [Make the "Let's Talk" link work on Enterprise pages](https://github.com/GooeyAI/gooey-server/commit/1bd676c6dc60f8fc760dcda7f46050a7ed1a2de6)

## 12-May-2026

**Fixed**

* [Retry on 504 timeout errors from Intron ASR](https://github.com/GooeyAI/gooey-server/commit/b13933dba65a205284b0d50e06cc5025c667ada1)

## 8-May-2026

**Fixed**

* [use call transfer tool for voice bots](https://github.com/GooeyAI/gooey-server/commit/ded22b70ec23161945ed1aa48b90303150419503)
* [avoid TypeError on ShortenedURL admin Add/Duplicate page](https://github.com/GooeyAI/gooey-server/commit/c43b5d1a85ed2bdb2205037f6a09467bd5647cb6)

## 7-May-2026

**Fixed**

* [IndexError: list index out of range](https://github.com/GooeyAI/gooey-server/commit/b7b76b26efada3f4e7c677222c578bebdc9bde13)
* [integrity error for yt-dlp metadata with unknown file size](https://github.com/GooeyAI/gooey-server/commit/2c7f3e84b27518676728d7af98598bae6682ee5d)
* [raw\_tts\_text cleanup for thinking traces](https://github.com/GooeyAI/gooey-server/commit/5afbd2415a5a26ee33a9b9c0a2ed76653c8aa060)

**Added**

* [Release Bot Builder for All](https://github.com/GooeyAI/gooey-server/commit/f6a4152c42da8f08119731158d07e68c659c8659)

## 5-May-2026

**Fixed**

* [keep file upload ON by default for new web integration](https://github.com/GooeyAI/gooey-server/commit/317c71d448aa135fd6ca68d14d3a03b4a02ff2ef)

## 4-May-2026

**Fixed**

* [set LiveKit Gemini Vertex requests to global region](https://github.com/GooeyAI/gooey-server/commit/5834d5dfc590f062725af893eeb5c8b37d0c3f05)

## 1-May-2026

**Added**

* [when filtering by workspace default sort should be last\_updated](https://github.com/GooeyAI/gooey-server/commit/130100bca2d70581614abbb94ddee0b99e5387df)

**Fixed**

* [handle openai swallowing task cancellation](https://github.com/GooeyAI/gooey-server/commit/c8b1611ab1dda5584ffd9b8344c4b96e728b95f1)

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
