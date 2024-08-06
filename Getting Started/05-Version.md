---
created: 2024-07-15T22:49:16 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Version

> ## Excerpt
> Specify which version of PORTA you use in your integration.

---
Last updated 2 months ago

In addition to an [access token][1], all requests must specify which version of the PORTA API they are accessing in the `accept-version` header. The example request below is for version 1:

```bash
curl '{baseUrl}/supplier/catalog/experiences' \ -H 'accept: application/json' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}'
```

Requests made without a valid API version will receive a 412 status code response:

```json
{ "code": "412", "id": "3ecae132-a32d-41f9-8f7d-586f34cc29ce", "message": "Missing accept-version header." }
```

At this time there is only one available version, `vnd.porta-api.v1`. This may change in the future.

[1]: https://porta.redoc.ly/getting-started/authentication/
