---
created: 2024-07-15T22:52:22 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Booking cancellation request

> ## Excerpt
> A PORTA booking cancellation request is sent when an order is cancelled by a customer.

---
Last updated 2 months ago

**Request endpoint**: `DELETE {supplier_url}/booking`

A booking cancellation request is usually sent when an order is cancelled by a customer.

A booking cancellation request contains the following properties:

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="booking_id"><span>booking_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;uuid&gt;</span></p><div><p>The ID of the booking to cancel.</p></div></div></td></tr><tr><td kind="field" title="ticket_numbers"><span>ticket_numbers</span><p>required</p></td><td><div><p><span>Array of </span><span>strings</span></p><div><p>A list of ticket values issued by the original booking confirmation response.</p></div></div></td></tr><tr><td kind="field" title="transaction_id"><span>transaction_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The ID issued by the original booking confirmation response.</p></div></div></td></tr></tbody></table>

## [][1]Timing out

If a booking confirmation request times out, the order is no longer considered valid. When this occurs, a cancellation request is sent one minute later with an `unconfirmed` property value of `true`. Suppliers are required to cancel the booking, regardless of the experience's cancellation policy.

[1]: https://porta.redoc.ly/getting-started/#timing-out
