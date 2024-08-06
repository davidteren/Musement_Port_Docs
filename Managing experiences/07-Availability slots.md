---
created: 2024-07-15T22:51:15 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Availability slots

> ## Excerpt
> Combine PORTA options and holder categories to create availability slots so that customers can book their experience.

---
Last updated 2 months ago

_Availability slots_ bring together all the components needed for a valid booking.

## [][1]Creating an availability slot

Suppliers must use the `POST /supplier/availability/experiences/{experience_id}/options/{option_id}/slots` endpoint to create an availability slot for an experience. The exact body of the request changes based on the [type][2] of slot the experience needs.

### [][3]Option

The `option_id` property must contain the ID of the [option][4] for the slot.

### [][5]Available holder categories

Every slot must contain a list of holder categories that are available for the slot in the `available_holder_categories` property. Each item must correspond to one of the option's holder categories and include its price (in cents).

The `min_quantity` property for an available holder category indicates the minimum pax number which must be selected for a valid booking. The `max_quantity` property indicates the maximum possible pax number which can be selected. When a maximum is not specified, no limit is enforced.

### [][6]Type

In addition to the properties described above, an availability slot will have additional properties depending on the `availability_slot_type` of the experience:

-   [Daily slot][7]
-   [Open slot][8]
-   [Time slot][9]

## [][10]Setting limits

The `capacity` property indicates the number of seats left for the availability slot. When the value is zero, the slot is no longer available. When this property is not provided, no seat limit is enforced.

Note that each pax number of holder categories in a booking will reduce the availability slot's remaining capacity. It is currently not possible to set a separate capacity for each holder category.

## [][11]Specifying languages

The `guide_languages` property lists languages which can be booked for the option and slot. This property is optional and can be skipped if there is no language component. The value must match the [ISO 639-1 standard][12].

[1]: https://porta.redoc.ly/getting-started/#creating-an-availability-slot
[2]: https://porta.redoc.ly/getting-started/#type
[3]: https://porta.redoc.ly/getting-started/#option
[4]: https://porta.redoc.ly/experiences/options/
[5]: https://porta.redoc.ly/getting-started/#available-holder-categories
[6]: https://porta.redoc.ly/getting-started/#type
[7]: https://porta.redoc.ly/experiences/availability-slots/daily/
[8]: https://porta.redoc.ly/experiences/availability-slots/open/
[9]: https://porta.redoc.ly/experiences/availability-slots/time/
[10]: https://porta.redoc.ly/getting-started/#setting-limits
[11]: https://porta.redoc.ly/getting-started/#specifying-languages
[12]: https://www.iso.org/iso-639-language-codes.html
