---
description: This section defines API keys and explains how to obtain them.
---

# Authentication

&#x20;ZAP API authenticates requests using API keys.

Your API keys provide access to all of your ZAP data. Please keep them safe as you would a password. We strongly advise you to use a password manager. Do not share your secret API keys in public places like GitHub, client-side code, and so on.

Bearer authentication is used to access the ZAP API. For example `curl -H "Authorization: Bearer <bearer token> .`Unless all API requests are authenticated, they will fail.





