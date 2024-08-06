---
created: 2024-07-15T22:51:48 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Hold availability

> ## Excerpt
> Use the PORTA hold availability request webhook to temporarily block availability in your system for potential orders.

---
Last updated 2 months ago

A hold availability request is sent to hold/block availability, ensuring that a future booking is guaranteed within a pre-defined period. This gives the customer a reasonable amount of time to add something to cart and complete details for checkout.

During the contracting phase, suppliers will agree to a `hold_duration` period for hold availability requests. Once this period has passed, a successful booking for the same availability is no longer guaranteed.

## [][1]Request and response

**Request endpoint**: `POST {supplier_url}/hold`

A hold availability request contains the following properties:

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="experience_id"><span>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The experience ID.</p></div></div></td></tr><tr><td kind="field" title="expiration_time"><span>expiration_time</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;date-time&gt;</span></p><div><p>When the hold availability request can expire, based on the agreed upon <code>hold_duration</code> value.</p><p>The value for this property must be in the local time for the experience with no time zone information, following the <a href="https://www.iso.org/iso-8601-date-and-time-format.html">ISO 8601 standard</a>.</p></div></div></td></tr><tr><td kind="field" title="hold_id"><span>hold_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;uuid&gt;</span></p><div><p>The ID of the hold availability request.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The option ID.</p></div></div></td></tr><tr><td kind="field" title="pickup_id"><span>pickup_id</span></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The pickup ID, if any.</p></div></div></td></tr><tr><td kind="field" title="quantities"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> <span>unique</span></span></p><div><p>An array of the requested holder categories and their quantities.</p></div></div></td></tr><tr><td kind="field" title="slot_id"><span>slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The availability slot ID.</p></div></div></td></tr></tbody></table>

The response to a successful hold availability request contains the following properties:

Hold availability request accepted

##### Response Schema: application/json

<table><tbody><tr><td kind="field" title="hold_id"><span>hold_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The hold ID from the request.</p></div></div></td></tr><tr><td kind="field" title="transaction_id"><span>transaction_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The supplier's own ID for the hold request.</p></div></div></td></tr></tbody></table>

## [][3]Capacity and quantity limits

Before a hold request is sent, PORTA validates the requested quantities against the following properties:

-   Option's `min_booking_quantity` and `max_booking_quantity`
-   Availability slot's `capacity`
-   Available holder category's `min_quantity` and `max_quantity`

If any of these properties are missing in PORTA, their validation is skipped. If any of the requested quantities is invalid, the requesting application receives an error and no hold availability request is sent to suppliers.

When setting up an experience, consider that some applications, like our own [musement.com][4], do not directly communicate quantity limits to customers. To reduce errors that customers may encounter while placing an order, consider avoiding limits to the capacity/quantities contained within an experience.

[1]: https://porta.redoc.ly/getting-started/#request-and-response
[2]: https://www.iso.org/iso-8601-date-and-time-format.html
[3]: https://porta.redoc.ly/getting-started/#capacity-and-quantity-limits
[4]: https://www.musement.com/
