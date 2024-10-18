# ✨ LLM-enabled Functions

## Where are LLM-enabled Functions useful?

There are many scenarios where we don't need to run the Functions for every Copilot query. For example:

* User wants to calculate data in between the conversation (like an HVAC CFM Calculation)
* LLM needs to do a Google search to respond to the query
* LLM needs to do a look-up weather API and answer the query&#x20;

<figure><img src="../../.gitbook/assets/pako_eNptkstugzAQRX9l5HXyAywqNSEkqdIu-tgUsrDwEKxim_qhNCL59w6GJKgqYoG5Z67njt2x0ghkCTtY3tbwnhYa6HnMPxxa4O7LAYfvgPa0h_n8ARbdbvdM_x32L8gKqqBLL40m0CJoRIHiMrgsqOSc3fRBO_c2y7y3sehao4WDo_T1zYh8DkGh9m4_2Czjzml-dQLpoORNg2Io_MunkV_defzBMni86quoZ3fdog-.png" alt="" width="492"><figcaption><p>A flowchart which shows the different flows </p></figcaption></figure>

## How do LLM-enabled Functions work?

When the user sends a query in Natural Language, the LLM determines the following:&#x20;

1. does the query require a function?
2. which part of the text should be passed as an argument in the function?

In the example below, the query is about CFM calculations which are commonly used in HVAC installations.&#x20;

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

## How to use LLM-enabled Functions?

Using LLM-enabled Functions is exactly the same as "BEFORE" and "AFTER" functions

### **Step 1** <a href="#step-1" id="step-1"></a>

Head over the [Functions workflow](https://gooey.ai/functions/)

### **Step 2** <a href="#step-2" id="step-2"></a>

Create your PROMPT Function:

* create a basic fetch call for the weather of any location
* create a serper&#x20;

**You can find more** [**examples here**](https://gooey.ai/functions/examples)

#### A basic Weather API call ([link here](https://gooey.ai/functions/current-weather-rxmquy60p1vq/))

```javascript
async ({ lat, long }) => {
  // Use Open-Meteo's public API for fetching weather data
  let url = `https://api.open-meteo.com/v1/forecast?latitude=${lat}&longitude=${long}&current_weather=true`;
  let response = await fetch(url);
  let data = await response.json();
  return { weather: data.current_weather };
};
```

#### An API call for serper  - a service for google search ([link here](https://gooey.ai/functions/google-search-without-api-key-tey6zrx2vzvm/))

```javascript
async ({ query }) => {
  var myHeaders = new Headers();
  myHeaders.append("X-API-KEY", "your API key");
  myHeaders.append("Content-Type", "application/json");
  
  var raw = JSON.stringify({
    "q": query
  });
  
  var requestOptions = {
    method: 'POST',
    headers: myHeaders,
    body: raw,
    redirect: 'follow'
  };
  
  let ret = await fetch("https://google.serper.dev/search", requestOptions);

  return { search_results: await ret.json() };
};

```

#### **Step 3** <a href="#step-3" id="step-3"></a>

Hit Submit, if your code is working fine you will get your outputs on the right side. Use the “Save as New” button and update the run name.

#### **Step 4** <a href="#step-5" id="step-5"></a>

Now head over to the Gooey workflow where you want to add the saved functions.

Head over to the example below:

{% embed url="https://gooey.ai/copilot/farmerchat-with-current-weather-data-qfzn662xf06v/" %}

Check the Functions option, and choose “PROMPT” from the dropdown and add your Saved example. And then hit "SUBMIT!

<figure><img src="../../.gitbook/assets/Screenshot 2024-10-19 at 1.03.32 AM.png" alt=""><figcaption></figcaption></figure>

_You can check your Functions output in the Workflow at the end of the page in "Details" section._

<figure><img src="https://docs.gooey.ai/~gitbook/image?url=https%3A%2F%2F662560811-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F5BFP5RUm6rTLXk8wUSTf%252Fuploads%252FenY8Js0Pe22WJWCN5Ook%252FScreenshot%25202024-08-09%2520at%25202.02.41%25E2%2580%25AFPM.png%3Falt%3Dmedia%26token%3D7386368f-50b3-4def-b495-977fcb610b40&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=c63c07c8&#x26;sv=1" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-10-19 at 1.15.29 AM.png" alt=""><figcaption></figcaption></figure>

