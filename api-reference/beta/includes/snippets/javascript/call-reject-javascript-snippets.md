---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const reject = {
  reason: "busy"
};

let res = await client.api('/app/calls/57dab8b1-894c-409a-b240-bd8beae78896/reject')
	.version('beta')
	.post(reject);

```