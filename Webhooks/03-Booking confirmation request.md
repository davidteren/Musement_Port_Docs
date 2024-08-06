---
created: 2024-07-15T22:52:16 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Booking confirmation request

> ## Excerpt
> Use the PORTA booking confirmation request webhook to record a paid order.

---
Last updated 2 months ago

**Request endpoint**: `POST {supplier_url}/booking`

A booking confirmation request is sent when a customer places a paid order.

A booking confirmation request contains the following properties:

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="booking_id"><span>booking_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The ID of the booking to confirm.</p></div></div></td></tr><tr><td kind="field" title="booking_requests"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> <span>unique</span></span></p><div><p>An array of items for the booking.</p></div></div></td></tr><tr><td kind="field" title="hold_id"><span>hold_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The ID of the availability hold request made when a customer added the item to cart.</p></div></div></td></tr><tr><td kind="field" title="holder"><p>required</p></td><td><div><p><span></span><span>object</span></p><div><p>Information about the lead booker.</p></div></div></td></tr><tr><td kind="field" title="tuimm_booking_id"><span>tuimm_booking_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^MUS[0-9]+?_[0-9]+?$</span></p><div><p>This property contains Musement booking information.</p><p>The value consists of two IDs separated by an underscore. The first ID, consisting of <code>MUS</code> and numbers, is the order ID to use when contacting Musement Customer Care.</p><p>The second ID, consisting only of numbers, is the ID for a single item in the order. This ID is used for internal technical checks and is not relevant when contacting Musement Customer Care.</p></div></div></td></tr></tbody></table>

The response to a successful booking confirmation request contains the following properties:

Booking confirmation request accepted

##### Response Schema: application/json

<table><tbody><tr><td kind="field" title="booking_id"><span>booking_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The booking ID from the request.</p></div></div></td></tr><tr><td kind="field" title="tickets"><p>required</p></td><td><div><p><span>Array of </span><span>Per person (object) or Per group (object)</span></p><div><p>An array of tickets that customers can use for their experience. Tickets can be unique per person in the booking or valid for the entire group.</p></div></div></td></tr><tr><td kind="field" title="transaction_id"><span>transaction_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The supplier's own ID for the booking request.</p></div></div></td></tr></tbody></table>

## [][1]Timing out

During initial registration negotiations, suppliers agree to webhook response time limits. If the supplier's webhook service takes too long to respond to a booking confirmation request, the booking is no longer considered valid. When this happens, PORTA automatically sends a [cancellation request][2]. In these situations, suppliers are required to cancel the booking, regardless of the experience's cancellation policy.

[1]: https://porta.redoc.ly/getting-started/#timing-out
[2]: https://porta.redoc.ly/webhooks/cancel/
