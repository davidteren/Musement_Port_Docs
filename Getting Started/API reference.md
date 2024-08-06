---
created: 2024-07-15T22:53:39 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# API reference

> ## Excerpt
> Documentation for managing your catalog on Musement via the PORTA API.

---
## PORTA (1.0.0)

Download OpenAPI specification:[Download][1]

## [][2]About PORTA

Musement's **PORTA** (_Perfect Open Road To Activities_) service allows suppliers to manage their experiences via API.

## [][3]Authentication

## [][4]Supplier-production

This is the default security scheme a supplier must use when accessing PORTA in the **production** environment.

**Security Scheme Type:** OAuth2

**Flow type:** `clientCredentials`

**Token URL:** `https://prod.api.tui/oauth2/token`

## [][5]Supplier-sandbox

This is the default security scheme a supplier must use when accessing PORTA in the **sandbox** environment.

**Security Scheme Type:** OAuth2

**Flow type:** `clientCredentials`

**Token URL:** `https://prod.api.tui/oauth2/token`

## [][6]Webhook

This security scheme is used by PORTA when calling a supplier's webhook service.

**Security Scheme Type:** API Key

**Header parameter name:** x-webhook-key

## [][7]Release notes

This section contains a record of changes to the API.

## [][8]2023-12-06

-   Added `unconfirmed` property to booking cancellation request webhook

## [][9]2023-10-12

-   Added `vendor_id` query parameter to the endpoint `GET /supplier/catalog/experiences`
    -   Filters results to those which belong to the specified vendor

## [][10]2023-10-02

-   Added `ticket_numbers` and `transaction_id` properties to booking cancellation request webhook

## [][11]2023-08-24

-   Changed `accept-version` header value used for webhook requests
    -   New value is `vnd.porta-webhook-api.v1`

## [][12]2023-06-22

-   Added webhook test endpoints for sandbox environment:
    -   `POST /supplier/integration-tests/book`
    -   `POST /supplier/integration-tests/cancel-booking`
    -   `POST /supplier/integration-tests/hold`

## [][13]2023-06-09

-   Added endpoint `PATCH /supplier/catalog/experiences/{experience_id}`
-   Added `archived` property to _Experience model_
    -   Archived experiences are no longer for sale

## [][14]2023-05-04

-   Removed `supplier-code` header parameter from all endpoints
-   Removed exhaust vent that exposed the Core

## [][15]2023-04-20

**Booking confirmation request**

-   Added `tuimm_booking_id` property
    -   Human-friendly Musement booking ID

**Vendors**

-   Added `Vendor` model
    -   Used to categorize experiences by different sources, partners or channels
-   Added two endpoints:
    -   `GET /supplier/vendors`
    -   `POST /supplier/vendors`
-   Added `vendor_id` property to _Experience model_

## [][16]2023-03-23

**Experience model**

-   Removed `content` and `media` properties

[1]: blob:https://porta.redoc.ly/d039549a-ee31-45b9-85df-284ae9f39396
[2]: https://porta.redoc.ly/getting-started/#section/About-PORTA
[3]: https://porta.redoc.ly/getting-started/#section/Authentication
[4]: https://porta.redoc.ly/getting-started/#Supplier-production
[5]: https://porta.redoc.ly/getting-started/#Supplier-sandbox
[6]: https://porta.redoc.ly/getting-started/#Webhook
[7]: https://porta.redoc.ly/getting-started/#section/Release-notes
[8]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-12-06
[9]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-10-12
[10]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-10-02
[11]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-08-24
[12]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-06-22
[13]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-06-09
[14]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-05-04
[15]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-04-20
[16]: https://porta.redoc.ly/getting-started/#section/Release-notes/2023-03-23
