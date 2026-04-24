---
description: Go through our Developer Alex's pro tips for using the AI Art QR Code API
---

# API tips on AI Art QR Code

## Question: I'm running the API but how do I add my own QR image?

### STEP 1:

You can click the first link on [gooey.ai/qr-code/api](https://gooey.ai/qr-code/api/) to see the [complete api documentation](https://api.gooey.ai/docs#operation/art-qr-code) with field names, response and request formats, etc.\
\
In this case what you are looking for is the <mark style="background-color:yellow;">qr\_code\_input\_image</mark> field which takes a file url corresponding to an existing qr code as a string:

<figure><img src="https://mail.google.com/mail/u/0?ui=2&#x26;ik=ff1edfb7df&#x26;attid=0.2&#x26;permmsgid=msg-f:1787054884674434599&#x26;th=18cce4f30b257627&#x26;view=fimg&#x26;fur=ip&#x26;sz=s0-l75-ft&#x26;attbid=ANGjdJ8KluvHmr76SUskx4CG5hV3XCPRghfuak4mDwSAIgNBiirjD6y-84Sm6VauEzajnbyPkT8sndDKO4NkOMPJzqiiqOYdr6kUlRDOCQgExVubsSnfAx2Bq520vNU&#x26;disp=emb&#x26;realattid=ii_lqsiyria3" alt=""><figcaption></figcaption></figure>

### STEP 2:

The easiest way to figure out how to format a specific request is to run it in the UI (e.g. upload an existing wifi QR code like this [https://gooey.ai/qr-code/?run\_id=v6lsozk6\&uid=2pZJQouaP2Okm18cbEhIpOQpqCg1](https://gooey.ai/qr-code/?run_id=v6lsozk6\&uid=2pZJQouaP2Okm18cbEhIpOQpqCg1)) hit submit and then go to the api tab. If you select "show all fields" and "python", it should give you the full api code to replicate the web ui run you are looking for:<br>

<figure><img src="https://mail.google.com/mail/u/0?ui=2&#x26;ik=ff1edfb7df&#x26;attid=0.1&#x26;permmsgid=msg-f:1787054884674434599&#x26;th=18cce4f30b257627&#x26;view=fimg&#x26;fur=ip&#x26;sz=s0-l75-ft&#x26;attbid=ANGjdJ9jRpbFKT3nj2nVYkG6T1tnPLY7diWrymjdVEZtJE8Y_562ngzwMJhp7ynt0kD-dzJAUqptr-6QU2PHfMKGBoe6P-4zR3IwPZYG9jDcQg8xhvXM5kgWi9ChKX0&#x26;disp=emb&#x26;realattid=ii_lqsix0do2" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="https://mail.google.com/mail/u/0?ui=2&#x26;ik=ff1edfb7df&#x26;attid=0.3&#x26;permmsgid=msg-f:1787054884674434599&#x26;th=18cce4f30b257627&#x26;view=fimg&#x26;fur=ip&#x26;sz=s0-l75-ft&#x26;attbid=ANGjdJ8uljRg3C_ohi41zoVN_MpuD9X_hVbyDYCKKK3fxM6eAvuHEhPG_HBHBQjJIkQnoHNL4fCECFRkczj6zpqZL9p97BIy9mNrm8ttm-Ds0pzBJKNX5iQHBfSUXrM&#x26;disp=emb&#x26;realattid=ii_lqsj0wun4" alt="" width="563"><figcaption></figcaption></figure>
