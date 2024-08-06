---
created: 2024-08-06T01:11:34 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# API reference

> ## Excerpt
> Documentation for managing your catalog on Musement via the PORTA API.

---
## PORTA (1.0.0)

Download OpenAPI specification:[Download](blob:https://porta.redoc.ly/9f2cc4b7-3b95-4065-96fd-2f642d509736)

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/About-PORTA)About PORTA

Musement's **PORTA** (_Perfect Open Road To Activities_) service allows suppliers to manage their experiences via API.

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Authentication)Authentication

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#Supplier-production)Supplier-production

This is the default security scheme a supplier must use when accessing PORTA in the **production** environment.

**Security Scheme Type:** OAuth2

**Flow type:** `clientCredentials`

**Token URL:** `https://prod.api.tui/oauth2/token`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#Supplier-sandbox)Supplier-sandbox

This is the default security scheme a supplier must use when accessing PORTA in the **sandbox** environment.

**Security Scheme Type:** OAuth2

**Flow type:** `clientCredentials`

**Token URL:** `https://prod.api.tui/oauth2/token`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#Webhook)Webhook

This security scheme is used by PORTA when calling a supplier's webhook service.

**Security Scheme Type:** API Key

**Header parameter name:** x-webhook-key

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes)Release notes

This section contains a record of changes to the API.

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-12-06)2023-12-06

-   Added `unconfirmed` property to booking cancellation request webhook

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-10-12)2023-10-12

-   Added `vendor_id` query parameter to the endpoint `GET /supplier/catalog/experiences`
    -   Filters results to those which belong to the specified vendor

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-10-02)2023-10-02

-   Added `ticket_numbers` and `transaction_id` properties to booking cancellation request webhook

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-08-24)2023-08-24

-   Changed `accept-version` header value used for webhook requests
    -   New value is `vnd.porta-webhook-api.v1`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-06-22)2023-06-22

-   Added webhook test endpoints for sandbox environment:
    -   `POST /supplier/integration-tests/book`
    -   `POST /supplier/integration-tests/cancel-booking`
    -   `POST /supplier/integration-tests/hold`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-06-09)2023-06-09

-   Added endpoint `PATCH /supplier/catalog/experiences/{experience_id}`
-   Added `archived` property to _Experience model_
    -   Archived experiences are no longer for sale

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-05-04)2023-05-04

-   Removed `supplier-code` header parameter from all endpoints
-   Removed exhaust vent that exposed the Core

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-04-20)2023-04-20

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

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#section/Release-notes/2023-03-23)2023-03-23

**Experience model**

-   Removed `content` and `media` properties
