---
created: 2024-07-15T22:51:07 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Daily slot

> ## Excerpt
> Daily slots in PORTA require customers to select a single date for a booking.

---
Last updated 2 months ago

A _daily slot_ requires customers to select a single date for a booking.

When an [availability slot][1] is daily, it must contain a `daily_slot` property with the bookable date. In the example response below, the slot is set up for 22 April 2023:

```json
{ [...], "daily_slot": { "date": "2023-04-22" }, [...] }
```

Dates are automatically assumed to match the local date of the experience location.

[1]: https://porta.redoc.ly/experiences/availability-slots/
