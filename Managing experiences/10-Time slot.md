---
created: 2024-07-15T22:51:32 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Time slot

> ## Excerpt
> Time slots in PORTA require customers to select both a date and time for a booking.

---
Last updated 2 months ago

A _time slot_ requires customers to select a date and time for a booking.

When an [availability slot][1] is time-based, it must contain a `time_slot` property with the bookable date and time. In the example response below, the slot is set up for 22 April 2023 at 6pm:

```json
{ [...], "time_slot": { "end": "2023-04-22T20:00:00Z", "start": "2023-04-22T18:00:00Z" }, [...] }
```

##### A note on time

Times in PORTA must be loaded for the local time of the experience. Do not adjust times for time zones or include time zone information.

## [][2]End time

A time slot must include an end date and time in the `end` property. In the example below, the slot is set to start at 6pm on 22 April 2023 and end two hours later:

```json
{ [...], "time_slot": { "end": "2023-04-22T20:00:00Z", "start": "2023-04-22T18:00:00Z" }, [...] }
```

The `end` property should reflect when the booked experience will end. If it does not have a well defined end time, we recommend to use the same value for both the start and end time:

```json
{ [...], "time_slot": { "end": "2023-04-22 18:00:00Z", "start": "2023-04-22 18:00:00Z" }, [...] }
```

Suppliers should be aware that this suggestion may change in the future.

## [][3]Pickups

Time slots support [pickup points][4]. The `pickup_ids` property lists the IDs of pickup points that are available for the slot. In the example response below, the slot contains a single pickup point:

```json
{ [...], "time_slot": { "end": "2023-04-22 20:00:00Z", "pickup_ids": [ "pickup-123" ], "start": "2023-04-22 18:00:00Z" }, [...] }
```

### [][5]How we do it

When selecting pickups and times on one of our distribution websites, like [musement.com][6], the start time of the time slot is shown. However, if a pickup point contains a `time_margin` value, the displayed time slot is modified to show the pickup time.

In the example screenshot below, the time slot is for 18:00, but the pickup's `time_margin` property value is `-15` (15 minutes before the time slot):

![pickup time](https://porta.redoc.ly/static/70f30cc6451a665a70648fd300569613/242e2/pickup-time.png "pickup time")

The modified time slot is limited to the Musement website, booking information and customer vouchers. The original time and `time_margin` remain unchanged in PORTA:

[1]: https://porta.redoc.ly/experiences/availability-slots/
[2]: https://porta.redoc.ly/getting-started/#end-time
[3]: https://porta.redoc.ly/getting-started/#pickups
[4]: https://porta.redoc.ly/experiences/pickups/
[5]: https://porta.redoc.ly/getting-started/#how-we-do-it
[6]: https://www.musement.com/
