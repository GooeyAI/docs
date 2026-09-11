# WhatsApp Rate Change Oct 2026

## What Meta is changing

Starting on October 1, 2026, Meta is changing their pricing structure for Service and Utility messages.

This change impacts any chatbots built using WhatsApp for message interface and delivery to users (whether built with [Gooey.AI](http://gooey.ai/) or not).

* Effective October 1, 2026 — Meta will charge on a per-message basis for all service messages, consistent with how Meta charges for template messages. These messages have not been charged since November 1, 2024.
* Effective October 1, 2026 — Meta will charge on a per-message basis for utility messages sent in response to users (within an open 24-hour customer service window). These messages have not been charged since July 1, 2025.

## What’s changing for Gooey Bots — Service Messages

Most customers use only Service Messages in [Gooey.AI](http://gooey.ai/) chatbots today. This communication will focus on service messages. Separately we will discuss utility messages as applicable.

### What’s a Service Message

A service message is a non-template response to a user. When a user starts a conversation with a Gooey chatbot via WhatsApp, that opens a Service conversation.

All of the responses from the Gooey bot to the user are “service messages” that will have a fee associated with them starting October 1st.

### How much does a Service Message cost?

Service message rates are determined by the country or region of the recipient of the message and are charged per message.

#### Location

For example, if a user in Kenya messages Farmer.Chat from a +254 Kenyan phone number on WhatsApp or a user in India messages from a +91 Indian phone number, the rates will differ based on location.

* India: service messages $0.0014 per message
* Kenya (“Rest of Africa” category per Meta): service messages $0.0040 per message

#### Per message

Each time the user asks a question and Farmer.Chat responds, that is a new service message. So if a user asks 3 questions and the bot replies 3 times, the 3 replies will be charged independently.

**Example: 3 user questions, 3 replies**

* India: $0.0014 per message X 3 reply messages = $0.0042
* Kenya: $0.0040 per message X 3 reply messages = $0.012

The full Meta rate card effective October 1, 2026 can be found here: [link](https://scontent-phl2-1.xx.fbcdn.net/v/t39.8562-6/790262948_2928535174159663_6336231100799892056_n.pdf?%5Fnc%5Fcat=106\&ccb=1-7&%5Fnc%5Fsid=b8d81d&%5Fnc%5Fohc=IRPedXTnd3EQ7kNvwGS3pN0&%5Fnc%5Foc=AdoeoJFNI%5FWAtlGjTrBAn-jmA4nvpodUCtIK2Og4gq3adDykkiCq6XOb4GAor5MR3lF3YFZ0RSn5lzdMGJfgSra%5F&%5Fnc%5Fzt=14&%5Fnc%5Fht=scontent-phl2-1.xx&%5Fnc%5Fgid=IuFh5mPcw2Zf3F%5Fjbq17Ow&%5Fnc%5Fss=7b289\&oh=00%5FAQIXQvtMBXNsoz8qD8sBMINiRb%5FO-PZGBOH-%5Fn9sAV9DWw\&oe=6A9E1CE0)

#### Rate updates — Meta document links

It’s worth noting that Meta publishes new rate cards quarterly, and both the rates and regions can change at that time.

Currently, Meta may update pricing only on the 1st day of each quarter, thus up to 4 times per year: January 1, April 1, July 1, and/or October 1.

* [https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing#pricing-calendar](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing#pricing-calendar)

Rate cards are always available on the Meta website:

* [https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing#rate-cards-and-volume-tiers](https://developers.facebook.com/documentation/business-messaging/whatsapp/pricing#rate-cards-and-volume-tiers)

### Calculating service message fees and where they appear

Typically customers go through two phases when launching a new chatbot with [Gooey.AI](http://gooey.ai/).

{% stepper %}
{% step %}
## Phase 1: Design, iteration, testing

In Phase 1, when building and iterating on a new chatbot, most customers leverage a Gooey Business Account WhatsApp number that Gooey provides for testing.

During this phase, customers will be charged for the WhatsApp fee via credits, similar to other shared service charges. (You can also opt to use your own number at this phase if you prefer.)
{% endstep %}

{% step %}
## Phase 2: Go-live launch with users

In Phase 2, when the customer is ready to launch their bot widely with their users, they obtain their own WhatsApp Business Account number and assign it to the bot in question.

Once you move to your own WhatsApp Business account, you will see the charges directly there.
{% endstep %}
{% endstepper %}

#### Reporting and transparency

We hope to partner with customers to provide as much transparency as possible into these new costs so that you can budget and track accordingly.

## What’s not changing

There is no change to the structure or requirements of the Service Messages themselves.

Users should not notice any difference in message style, length, delivery or latency, as long as there is no shortage of credits for your WhatsApp number.
