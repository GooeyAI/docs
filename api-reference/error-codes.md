# Error Codes

If you are facing some errors in your API and SDK calls, you may encounter some "error codes" in the response. Have a look at the error codes to know more:

## API Errors

<table><thead><tr><th width="254">Error Code</th><th>Overview</th></tr></thead><tbody><tr><td>401 API key not provided / banned</td><td><p><strong>Cause</strong>: Invalid Authentication</p><p><strong>Solution</strong>: Ensure the <a href="https://gooey.ai/account/api-keys/">correct API key</a> and requesting organization is being used.<br><br>Or </p><p><br><strong>Cause</strong>: You are banned from using Gooey.AI’s API</p></td></tr><tr><td>402 Payment Required</td><td><p><strong>Cause</strong>: Insufficient credits</p><p><strong>Solution</strong>: Ensure you have sufficient credits to run the API call. You can add <a href="https://gooey.ai/account/">more credits to your account</a>.</p></td></tr><tr><td>403 Invalid API Key </td><td><p><strong>Cause</strong>: The requesting API key is not correct.</p><p><strong>Solution</strong>: Ensure the API key used is correct, clear your browser cache, or <a href="https://gooey.ai/account/api-keys/">generate a new one</a>.</p></td></tr><tr><td>422 Validation Error</td><td><p><strong>Cause</strong>: Your request was malformed or missing some required parameters, such as a token or an input.</p><p><strong>Solution</strong>: The error message should advise you on the specific error made. Check the <a href="https://api.gooey.ai/docs">API documentation</a> for the specific API method you are calling and make sure you are sending valid and complete parameters. You may also need to check the encoding, format, or size of your request data.</p></td></tr><tr><td>429 Too Many Requests</td><td><strong>Cause</strong>: You have exceeded your rate limits<br><strong>Solution</strong>: Pace your requests. Read the <a href="https://docs.gooey.ai/api-reference/rate-limits">Rate limit guide</a>. </td></tr><tr><td>500 Internal Server Error</td><td><p><strong>Cause</strong>: Issue on our servers.</p><p><strong>Solution</strong>: Retry your request after a brief wait and contact us if the issue persists. Check the <a href="https://status.gooey.ai/">status page</a>.</p></td></tr></tbody></table>

## Handling Errors

We recommend that you programmatically handle errors. Here is an example to ensure that you can get the error codes in your console/environment

In the code snippet below the line `if (!response.ok) { throw new Error(response.status); }` provides the error codes in your console/environment.&#x20;

```javascript
import fetch from 'node-fetch';

const payload = {
  "search_query": "what are f-strings?",
  "documents": [
    "https://static.realpython.com/python-basics-sample-chapters.pdf",
    "https://edu.anarcho-copy.org/Programming%20Languages/Python/Automate%20the%20Boring%20Stuff%20with%20Python.pdf"
  ]
};

async function gooeyAPI() {
  const response = await fetch("https://api.gooey.ai/v2/doc-search", {
    method: "POST",
    headers: {
      "Authorization": "Bearer " + process.env["GOOEY_API_KEY"],
      "Content-Type": "application/json",
    },
    body: JSON.stringify(payload),
  });

  if (!response.ok) {
    throw new Error(response.status);
  }

  const result = await response.json();
  console.log(response.status, result);
}

gooeyAPI();
```
