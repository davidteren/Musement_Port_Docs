---
created: 2024-07-15T22:52:28 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Health check

> ## Excerpt
> PORTA makes a regular health check request to ensure that your integration is working as expected.

---
Last updated 2 months ago

**Request endpoint**: `GET {supplier_url}/heath`

PORTA will call the webhook service approximately every five minutes to verify its status. A non-200 status code response could lead to temporarily disabling products in the Musement catalog until the supplier's service is restored.
