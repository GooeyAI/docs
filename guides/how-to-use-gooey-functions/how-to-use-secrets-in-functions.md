---
icon: key-skeleton
---

# How to use SECRETS in Functions?

Our main aim with Functions is to allow users to chain API calls and connect their other services to Gooey.AI's workflows. Several services like Supabase, Firebase and more require their own API keys. Now you can store them in your [API Keys tab](https://gooey.ai/account/api-keys/) in the Accounts Page.&#x20;

### Step 1

Head over to [Gooey.AI Functions](https://gooey.ai/functions)

### **Step 2**

Set up your API call. In this example, we'll create an API call to Open Weather Map, so that it can share real-time weather stats with the user.&#x20;

```javascript
async ({ city_name }) => {
  const API_KEY = process.env.YOUR_API_KEY;
  if (!API_KEY) throw new Error("API key not found in environment variables.");
  const encodedCityName = encodeURIComponent(city_name);
  const response = await fetch(`https://api.openweathermap.org/data/2.5/weather?q=${encodedCityName}&appid=${API_KEY}&units=metric`);
  if (!response.ok) throw new Error(`Error ${response.status}: ${response.statusText}`);
  return { weather_data: await response.json() };
};
```

Here `process.env.YOUR_API_KEY` calls the secret key from your "Secrets".&#x20;

### Step 3

Scroll down to the "Secrets" section in the Functions Workflow. Select the API you need for this function to work successfully. &#x20;

<figure><img src="../../.gitbook/assets/Screen Recording 2025-01-06 at 3.00.32 PM processed.gif" alt=""><figcaption></figcaption></figure>

### Step 4

Hit "Run" and Save the function.&#x20;

{% hint style="info" %}
NOTE:  Before saving the workflow check if your response output is correct.
{% endhint %}

### Step 5

Add the saved Functions workflow in AI Copilot or other Gooey.AI Workflows.&#x20;

<figure><img src="../../.gitbook/assets/Screen Recording 2025-01-06 at 3.15.23 PM processed.gif" alt=""><figcaption></figcaption></figure>

***



Learn more about adding SECRETS to your Workspaces here:

{% embed url="https://docs.gooey.ai/guides/how-to-use-workspaces/how-to-add-secrets-in-your-workspace" %}



