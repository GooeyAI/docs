# Sending Targeted Messages with the Broadcast API

The Broadcast API can send a message to one user, not only to every user in an integration.

`integration_id` selects the bot integration. `filters` narrows the recipient list inside that integration.

caution If you omit `filters`, the message is sent to all conversations/users for that integration. Always include a phone-number filter for one-user sends.

If the phone number does not match an existing conversation in that integration, the API returns a `404` and does not send the message.

### Example Request

```http
POST https://api.gooey.ai/v2/agent/broadcast/send/
Authorization: Bearer <GOOEY_API_KEY>
Content-Type: application/json
```

```json
{
  "text": "Welcome! I'm your assistant.",
  "integration_id": "your-integration-id",
  "filters": {
    "wa_phone_number__in": ["+91XXXXXXXXXX"]
  }
}
```

Response:

```json
{
  "status": "success",
  "count": 1
}
```

Use E.164 phone format, for example `+919876543210`.

### Sending Files

The same endpoint accepts file URLs through `audio`, `video`, and `documents`.

```json
{
  "text": "Your report is ready.",
  "integration_id": "your-integration-id",
  "documents": ["https://example.com/report.pdf"],
  "filters": {
    "wa_phone_number__in": ["+91XXXXXXXXXX"]
  }
}
```

This is useful when a backend job or Gooey Function generates a PDF, audio file, video, or other downloadable asset. Once the file URL is available, call the Broadcast API and scope the send to the user with `filters`.

### Using a Gooey Function

If an agent needs to trigger the message, create a Gooey Function that calls `/agent/broadcast/send/`. The agent can pass the `integration_id`, target phone number, message text, and optional file URL to the function.

```js
async ({ integration_id, phone_number, text, file_url }) => {
  const phoneNumber = phone_number.replace(/\s/g, "");

  const payload = {
    text,
    integration_id,
    filters: {
      // For Twilio-backed SMS/MMS, use twilio_phone_number__in instead.
      wa_phone_number__in: [phoneNumber]
    }
  };

  if (file_url) {
    payload.documents = [file_url];
  }

  const res = await fetch("https://api.gooey.ai/v2/agent/broadcast/send/", {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
      "Authorization": `Bearer ${process.env.GOOEY_API_KEY}`
    },
    body: JSON.stringify(payload)
  });

  if (!res.ok) {
    throw new Error(await res.text());
  }

  return await res.json();
};
```

For audio or video files, use `audio: file_url` or `video: file_url` instead of `documents`.

Use the filter key that matches your integration type.

### WhatsApp 24-Hour Window

WhatsApp only allows outbound messages within 24 hours of the user's last message to your integration. If a broadcast does not arrive, check whether the recipient has messaged the integration in the last 24 hours. If not, ask them to send a message first, then retry.
