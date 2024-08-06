---
created: 2024-07-17T16:13:40 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/webhooks/
author: 
---

# Webhooks

> ## Excerpt
> Create a webhook service for PORTA so that you can sync your availability with ours.

---
Last updated 2 months ago

Suppliers must set up a webhook service to receive requests from PORTA related to bookings.

## [][1]Authentication

PORTA will send requests to the supplier's webhook service endpoint with a pre-defined `x-webhook-key` header value.

## [][2]Requests

PORTA currently makes the following webhook requests:

-   [Hold availability][3]
    -   `POST {supplier_url}/hold`
-   [Booking confirmation][4]
    -   `POST {supplier_url}/booking`
-   [Cancel booking][5]
    -   `DELETE {supplier_url}/booking`
-   [Health check][6]
    -   `GET {supplier_url}/heath`

## [][7]Error responses

If a request is not successful for any reason, the webhook response must be a 400 status code with one of the following error messages in the response's `code` property:

-   `ELEMENT_NOT_FOUND`
    -   One or more of the IDs in the request are not recognized
-   `INACTIVE_HOLD_KEY`
    -   When attempting to confirm a booking for an expired hold
-   `INACTIVE_OR_UNAVAILABLE_EXPERIENCE`
    -   The experience is no longer available
-   `INCORRECT_REQUEST`
    -   The request contains errors
-   `NO_CAPACITY_LEFT`
    -   There are no more free seats available
-   `NOT_CANCELLABLE_BOOKING`
    -   When attempting to cancel a booking that can no longer be cancelled
-   `UNCLASSIFIED_ERROR`
    -   The error does not match any of the other cases
-   `VALIDATION_ERROR`
    -   One or more of the properties (for example mandatory answers) does not match the expected type/format

[1]: https://porta.redoc.ly/webhooks/#authentication
[2]: https://porta.redoc.ly/webhooks/#requests
[3]: https://porta.redoc.ly/webhooks/hold/
[4]: https://porta.redoc.ly/webhooks/confirm/
[5]: https://porta.redoc.ly/webhooks/cancel/
[6]: https://porta.redoc.ly/webhooks/health/
[7]: https://porta.redoc.ly/webhooks/#error-responses
