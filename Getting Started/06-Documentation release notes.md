---
created: 2024-07-15T22:49:37 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Documentation release notes

> ## Excerpt
> A record of all major changes to the PORTA documentation.

---
[![](https://porta.redoc.ly/images/logo-light.png)][1]

Last updated 2 months ago

This page describes major changes to information in the PORTA documentation. For changes in the API, refer to the release notes in the [API reference][2].

## [][3]2024-04-17

-   Corrected information about dates and times
    -   Corrected example for [open slots][4]
    -   Added note about correct format for [time slots][5]
    -   Updated example time values in [OpenAPI spec][6] to match expected format

## [][7]2024-03-08

-   Updated information in [OpenAPI spec][8]
    -   Specified `slot_id` property value for availability slots cannot be re-used in other experiences
    -   Specified `guide_languages` appear for all available holders in availability slot
    -   Updated information about `mandatory_answers` property in [booking confirmation webhook][9]
    -   Refined `expiration_time` example value for [hold availability webhook][10]
    -   Removed `guide_language` property from [booking confirmation webhook][11]

## [][12]2024-01-12

-   Added missing endpoint example to [availability slots page][13]
-   Corrected error in [OpenAPI spec][14] and [guide][15] regarding time slots
    -   The `end` property is _required_

## [][16]2023-12-06

-   Added `unconfirmed` property to [booking cancellation request webhook][17]

## [][18]2023-11-15

-   Corrected errors in [OpenAPI spec][19] for webhook booking confirmation response
    -   Removed non-existent `mimeType` property from `FOR_SINGLE_PERSON` tickets
    -   Removed non-existent `URL` enum from `format` property for `FOR_SINGLE_PERSON` tickets

## [][20]2023-10-24

-   Corrected errors regarding [open slots][21]

## [][22]2023-10-20

-   Changes to [webhook testing page][23]
    -   Added diagram of testing flow
    -   Corrected errors regarding testing endpoint responses
    -   Modified OpenAPI spec to highlight differences between testing requests and webhook requests

## [][24]2023-10-12

-   Added [details][25] about the `vendor_id` query parameter for the endpoint `GET /supplier/catalog/experiences`
-   Corrections for the [webhook cancellation test endpoint][26]
    -   Added missing request body properties
    -   Updated response details

## [][27]2023-10-02

-   Corrected sandbox authentication URL in the [OpenAPI spec][28]
-   Added [webhook][29] endpoints

## [][30]2023-07-14

-   Changed email on [_Contact us_ page][31]
-   Added email to the [OpenAPI spec][32]

## [][33]2023-06-22

-   Added [sandbox environment][34] information
-   Added [webhook testing][35] page
    -   Endpoints are only available for sandbox environment
-   Updated the [OpenAPI spec][36] security requirements to indicate which endpoints are available by environment

## [][37]2023-06-09

-   Added two sections for [experiences][38] :
    -   [Archiving experiences][39]
    -   [Updating experiences][40]

## [][41]2023-05-04

-   Removed _Supplier code_ page
-   Removed `supplier-code` header from all request examples

## [][42]2023-04-20

-   Added _Documentation release notes_ page
-   Added page for [vendors][43]
-   Added clarification about [pickup times][44] on Musement distribution sites
-   Added clarification about capacity/quantity limits for [hold availability webhook requests][45]
-   Removed capital letters from ID examples

## [][46]2023-03-23

-   Removed pages describing business platform configurations in PORTA. This information will be managed by the _Content Supplier Connectivity_ team

Navigated to Documentation release notes

[1]: https://porta.redoc.ly/
[2]: https://porta.redoc.ly/openapi/overview/
[3]: https://porta.redoc.ly/getting-started/#2024-04-17
[4]: https://porta.redoc.ly/experiences/availability-slots/open/
[5]: https://porta.redoc.ly/experiences/availability-slots/time/
[6]: https://porta.redoc.ly/openapi/overview/
[7]: https://porta.redoc.ly/getting-started/#2024-03-08
[8]: https://porta.redoc.ly/openapi/overview/
[9]: https://porta.redoc.ly/webhooks/confirm/
[10]: https://porta.redoc.ly/webhooks/hold/
[11]: https://porta.redoc.ly/webhooks/confirm/
[12]: https://porta.redoc.ly/getting-started/#2024-01-12
[13]: https://porta.redoc.ly/experiences/availability-slots/
[14]: https://porta.redoc.ly/openapi/overview/
[15]: https://porta.redoc.ly/experiences/availability-slots/time/
[16]: https://porta.redoc.ly/getting-started/#2023-12-06
[17]: https://porta.redoc.ly/webhooks/cancel/
[18]: https://porta.redoc.ly/getting-started/#2023-11-15
[19]: https://porta.redoc.ly/openapi/overview/
[20]: https://porta.redoc.ly/getting-started/#2023-10-24
[21]: https://porta.redoc.ly/experiences/availability-slots/open/
[22]: https://porta.redoc.ly/getting-started/#2023-10-20
[23]: https://porta.redoc.ly/webhooks/testing/
[24]: https://porta.redoc.ly/getting-started/#2023-10-12
[25]: https://porta.redoc.ly/experiences/vendors/
[26]: https://porta.redoc.ly/webhooks/testing/#booking-cancellation
[27]: https://porta.redoc.ly/getting-started/#2023-10-02
[28]: https://porta.redoc.ly/openapi/overview/
[29]: https://porta.redoc.ly/webhooks/
[30]: https://porta.redoc.ly/getting-started/#2023-07-14
[31]: https://porta.redoc.ly/contact-us/
[32]: https://porta.redoc.ly/openapi/overview/
[33]: https://porta.redoc.ly/getting-started/#2023-06-22
[34]: https://porta.redoc.ly/getting-started/environments/
[35]: https://porta.redoc.ly/webhooks/testing/
[36]: https://porta.redoc.ly/openapi/overview/
[37]: https://porta.redoc.ly/getting-started/#2023-06-09
[38]: https://porta.redoc.ly/experiences/
[39]: https://porta.redoc.ly/experiences/#archiving-an-experience
[40]: https://porta.redoc.ly/experiences/#updating-an-experience
[41]: https://porta.redoc.ly/getting-started/#2023-05-04
[42]: https://porta.redoc.ly/getting-started/#2023-04-20
[43]: https://porta.redoc.ly/experiences/vendors/
[44]: https://porta.redoc.ly/experiences/availability-slots/time/
[45]: https://porta.redoc.ly/webhooks/hold/
[46]: https://porta.redoc.ly/getting-started/#2023-03-23
