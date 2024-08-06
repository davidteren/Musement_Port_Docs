---
created: 2024-07-15T22:53:23 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Testing

> ## Excerpt
> Test your integration by triggering webhook requests in PORTA's sandbox environment.

---
Last updated 2 months ago

The sandbox environment includes additional endpoints for testing webhooks. Sending a request to these endpoints transforms it into a request for your webhook service. Using these endpoints allows suppliers to test their integration before going live.

The request bodies must contain most of the same properties expected for real requests. Suppliers need to generate values for some properties, while others should come from existing properties in the sandbox environment.

Properties used across multiple webhook requests must contain consistent values. Generated values cannot always be completely random.

## [][1]Hold availability

You can send yourself a hold availability request in the sandbox environment at `POST /supplier/integration-tests/hold`:

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="experience_id"><span>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID for an existing sandbox experience.</p></div></div></td></tr><tr><td kind="field" title="expiration_time"><span>expiration_time</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;date-time&gt;</span></p><div><p>When the hold availability request can expire, based on the agreed upon <code>hold_duration</code> value.</p><p>The value for this property must be in the local time for the experience with no time zone information, following the <a href="https://www.iso.org/iso-8601-date-and-time-format.html">ISO 8601 standard</a>.</p></div></div></td></tr><tr><td kind="field" title="hold_id"><span>hold_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;uuid&gt;</span></p><div><p>A randomly-generated UUID. The same <code>hold_id</code> value must be used when testing the booking confirmation webhook.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID for an existing sandbox option.</p></div></div></td></tr><tr><td kind="field" title="pickup_id"><span>pickup_id</span></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID for an existing sandbox pickup, if any.</p></div></div></td></tr><tr><td kind="field" title="quantities"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> <span>unique</span></span></p><div><p>An array of the requested holder categories and their quantities.</p></div></div></td></tr><tr><td kind="field" title="slot_id"><span>slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID for an existing sandbox availability slot.</p></div></div></td></tr></tbody></table>

A valid request returns an empty 200 status code response. Request errors return a 400 status code response.

## [][3]Booking confirmation

You can send yourself a booking confirmation request at `POST /supplier/integration-tests/book`:

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="booking_id"><span>booking_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;uuid&gt;</span></p><div><p>A randomly-generated UUID. The same <code>booking_id</code> value must be used when testing the booking cancellation webhook.</p></div></div></td></tr><tr><td kind="field" title="booking_requests"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> <span>unique</span></span></p><div><p>An array of items for the booking.</p></div></div></td></tr><tr><td kind="field" title="hold_id"><span>hold_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The ID of the sandbox hold availability request.</p></div></div></td></tr><tr><td kind="field" title="holder"><p>required</p></td><td><div><p><span></span><span>object</span></p><div><p>Randomly-generated lead booker information.</p></div></div></td></tr><tr><td kind="field" title="pickup_id"><span>pickup_id</span></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID of an existing sandbox pickup, if any.</p><p>Note that the location of this property differs from its location in the confirmation request sent to your webhook service.</p></div></div></td></tr><tr><td kind="field" title="slot_id"><span>slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID of an existing sandbox availability slot.</p><p>Note that the location of this property differs from its location in the confirmation request sent to your webhook service.</p></div></div></td></tr><tr><td kind="field" title="request_id"><span>request_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;uuid&gt;</span></p><div><p>In production this property reflects PORTA's own ID for the item in the webhook request. Here, it can be a randomly-generated UUID. The same <code>request_id</code> value will appear in the request sent to the webhook service.</p><p>Note that the location of this property differs from its location in the confirmation request sent to your webhook service.</p></div></div></td></tr></tbody></table>

Please note that the request for this endpoint differs from the request that is eventually sent to the webhook service. The following properties in this request are moved to each item in the `booking_requests` property:

-   `request_id`
-   `guide_language`
-   `pickup_id` (if present)
-   `slot_id`

A randomly-generated value for `tuimm_booking_id` is also added to the final request that the webhook service receives.

A valid request returns an empty 200 status code response. Request errors return a 400 status code response.

## [][4]Booking cancellation

You can trigger a booking cancellation request at `POST /supplier/integration-tests/cancel-booking`:

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="booking_id"><span>booking_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;uuid&gt;</span></p><div><p>The ID of the booking to cancel.</p></div></div></td></tr><tr><td kind="field" title="ticket_numbers"><span>ticket_numbers</span><p>required</p></td><td><div><p><span>Array of </span><span>strings</span></p><div><p>A list of ticket values issued by the original booking confirmation response.</p></div></div></td></tr><tr><td kind="field" title="transaction_id"><span>transaction_id</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The ID issued by the original booking confirmation response.</p></div></div></td></tr></tbody></table>

A valid request returns an empty 200 status code response. Request errors return a 400 status code response.

[1]: https://porta.redoc.ly/getting-started/#hold-availability
[2]: https://www.iso.org/iso-8601-date-and-time-format.html
[3]: https://porta.redoc.ly/getting-started/#booking-confirmation
[4]: https://porta.redoc.ly/getting-started/#booking-cancellation
