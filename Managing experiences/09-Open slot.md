---
created: 2024-07-15T22:51:27 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Open slot

> ## Excerpt
> Open slots in PORTA give customers a booking that is valid for a set amount of time.

---
Last updated 2 months ago

An _open slot_ automatically provides customers with a booking that is valid for a set amount of time.

The exact expiration date depends on the [availability slot's][1] `open_slot` property.

## [][2]Duration days

When a booking is valid for a set number of days after purchase, the open slot's `type` property value is `DURATION_DAYS`. The slot should contain a `duration_days` property with the exact number of days.

In the example response below, the open slot is valid for 180 days after purchase:

```json
{ [...], "open_slot": { "duration_days": 180, "type": "DURATION_DAYS" }, [...] }
```

## [][3]End date

When all bookings must expire on a specific date, the open slot's `type` property value is `END_DATE`. The slot must contain an `end_date` property with the expiration date.

In the example response below, the open slot expires on 23 April 2023:

```json
{ [...], "open_slot": { "end_date": "2023-04-23", "type": "END_DATE" }, [...] }
```

[1]: https://porta.redoc.ly/experiences/availability-slots/
[2]: https://porta.redoc.ly/getting-started/#duration-days
[3]: https://porta.redoc.ly/getting-started/#end-date
