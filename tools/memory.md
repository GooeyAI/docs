---
icon: server
---

# Memory

You can make your \`Functions\` step remember information between runs when it is used inside a Copilot with Memory enabled.

### **Why do we need memory**

\- Your function can read saved memory

\- Your function can update saved memory

\- Changes are saved after the function finishes

### **How it works**

1\. In your Copilot, enable a Gooey Memory tool.

2\. Add a \`Functions\` workflow step/hook to that same bot.

3\. Run the bot as usual.

<mark style="background-color:blue;">**If Memory is enabled on the bot, your function will automatically receive it.**</mark>

Try these examples:

{% embed url="https://gooey.ai/copilot/functions-readwrite-memory-demo-for-agents-5330zy7cxwty/" %}

{% embed url="https://gooey.ai/functions/memory-readwrite-from-functions-98o4jo5ghwpc/" %}

#### How to use it in JavaScript

Use the global `GOOEY_MEMORY` object.

```javascript
(vars) => {
  GOOEY_MEMORY.user_name = vars.name;
  GOOEY_MEMORY.last_seen_at = new Date().toISOString();
  GOOEY_MEMORY.last_topic = vars.topic;
  return {
    saved: true,
    last_seen_at: GOOEY_MEMORY.last_seen_at
  };
}
```

#### How to use it in Python

Use the global \`GOOEY\_MEMORY\` object.

```python
from datetime import datetime, timezone

def main(name: str, topic: str, **kwargs):
    GOOEY_MEMORY["user_name"] = name
    GOOEY_MEMORY["last_seen_at"] = datetime.now(timezone.utc).isoformat()
    GOOEY_MEMORY["last_topic"] = topic
    
    return {
        "saved": True,
        "last_seen_at": GOOEY_MEMORY["last_seen_at"],
    }

```

#### Deleting a memory value (optional)

**JavaScript:**

```javascript
delete GOOEY_MEMORY.temp_value;
```

**Python:**

```python
GOOEY_MEMORY.pop("temp_value", None)
```

#### Good use cases

\- Save a user’s name

\- Save a preferred language

\- Save the last selected option

\- Save the last topic discussed

\- Save a last-seen timestamp

\- Save simple flags like `onboarding_complete = true`

#### Important notes

\- Memory is only available automatically when the function is run from a copilot with Memory enabled.

\- Changes are saved after the function completes.

\- This memory works best for “latest value” style data (for example, last seen time, preferences, or status flags).

#### Troubleshooting

\- If `GOOEY_MEMORY` seems empty, make sure the Copilot Memory Integration is enabled.

\- If changes are not saved, check whether the function run failed with an error.

<br>
