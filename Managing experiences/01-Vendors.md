
---
created: 2024-07-15T22:49:57 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author:
---

# Vendors

> ## Excerpt
> Learn how to create a vendor for your experiences in PORTA.

---
Last updated 2 months ago

Vendors allow suppliers to separate experiences with different sources, partners and/or channels.

Since a vendor is required when creating an [experience][1] in PORTA, new suppliers need to create a vendor first:

```bash
curl '{baseUrl}/supplier/vendors' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "name": "Supplier Tours Inc", "vendor_id": "vendor-123" }'
```

Suppliers who source the experience themselves, or do not have different channels, can create a vendor with their own name.

You can filter experiences in PORTA by a specific vendor using the `vendor_id` query parameter with the `GET /supplier/catalog/experiences` endpoint:

```bash
curl '{baseUrl}/supplier/catalog/experiences?vendor_id=vendor-123' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json'
```

[1]: https://porta.redoc.ly/experiences/
