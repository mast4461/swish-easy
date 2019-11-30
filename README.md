# swish-easy
A tiny website for prefilled swish payments. Create a link and send it to someone and they can open Swish with the payment details you specified prefilled.

On mobile they can simply click a link to open Swish.

If not on mobile they can scan the QR code from Swish.

Ambition: Make something simple that works.

## Create URLs programmatically

You can create your own hashes for the URL programmatically:
1. Put your data in JSON according to [this JSON schema](./url-data.schema.json).
2. JSON stringify the data.
3. Base 64 encode the data.
4. URL encode the data.

For example, in the browser: 
```
urlHash = encodeURIComponent(btoa(JSON.stringify(data)));
```

_(In case this README is outdated, have a look at the code in [index.html](./index.html), or maybe just copy it)_
