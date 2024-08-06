# 🧩 How to use Gooey Functions?

In this guide, we will look at the steps of creating a functions call on Gooey.AI and adding it to our Gooey.AI workflows.&#x20;

### **Step 1**

Head over the [Functions workflow](https://gooey.ai/functions/)

### **Step 2**

Create your POST Request with AFTER Function

{% code title="A basic fetch call" lineNumbers="true" %}
```javascript
async (variables) => {
  const res = await fetch("https://httpbin.org/post", {
    method: "POST",
    body: JSON.stringify(variables),
    headers: {
      "Content-Type": "application/json",
    },
  });
  return { response: await res.json() };
};
```
{% endcode %}

**Currently, we have added httpbin for our POST request, you can change this for your preferred API.**

<figure><img src="../.gitbook/assets/Functions Article (1).jpg" alt=""><figcaption></figcaption></figure>

### **Step 3**

Add your relevant variables

<figure><img src="../.gitbook/assets/variables.gif" alt="" width="375"><figcaption></figcaption></figure>

### **Step 4**

Hit Submit, if your code is working fine. Use the “Save as New” button and update the run name.

<figure><img src="../.gitbook/assets/saveasnew.gif" alt=""><figcaption></figcaption></figure>

### **Step 5**

Now head over to the Gooey workflow where you want to add the saved functions.

Head over to the example below:&#x20;

{% embed url="https://gooey.ai/compare-large-language-models/gooey-bot-chat-analysis-script-27lrilywfzmv/" %}

<figure><img src="../.gitbook/assets/Screenshot 2024-08-06 at 11.36.19 AM.png" alt=""><figcaption></figcaption></figure>

Check the Functions, choose “AFTER” and add your Saved example. And then hit "SUBMIT!&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2024-08-06 at 11.36.19 AM (1).png" alt=""><figcaption></figcaption></figure>

You can check your Functions output in the Workflow at the end of the page in "Details" section.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2024-08-06 at 11.20.55 PM.png" alt=""><figcaption></figcaption></figure>

### How do I find all the available functions and how can I contribute? <a href="#id-86mplbjxoi5t" id="id-86mplbjxoi5t"></a>

All the functions are available here:

{% embed url="https://gooey.ai/functions/examples/" %}

Choose any of the Examples and Fork them!

<figure><img src="../.gitbook/assets/examplesection.gif" alt=""><figcaption></figcaption></figure>
