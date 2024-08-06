---
created: 2024-07-15T22:50:59 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Pickup points

> ## Excerpt
> Collect your customers from pickup locations loaded into PORTA.

---
Last updated 2 months ago

In the Musement catalog, experiences with _pickup points_ require customers to select a pickup location _before selecting a date_. This is useful for situations where the dates and prices can vary by pickup location.

If nothing varies for your pickups, consider setting up pickups as [mandatory questions][1] instead so that they appear near the end of the booking flow.

When an experience contains pickups, selecting a pickup is required to complete a booking. However, pickups are optional for experiences and suppliers can skip this step if they don't plan to use them.

## [][2]Creating a pickup

You only need to create a pickup location once. It can be used again for multiple experiences.

```bash
curl -X POST '{baseUrl}/supplier/catalog/pickups' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "latitude": 39.65577, "longitude": 3.43884, "name": "Taxi stop hotel melbeach", "pickup_id": "pickup-123", "type": "MEETING_POINT" }'
```

The following properties are required for new pickup points:

### [][3]`pickup_id`

Suppliers must provide their own ID for a pickup. This ID will be used for relevant endpoints and requests.

### [][4]`name`

Give the pickup point a name in English that customers will use during booking.

### [][5]`type`

This property specifies whether the pickup point is a general location or the lobby of a hotel:

-   `HOTEL`
    -   The pickup is at a hotel.
-   `MEETING_POINT`
    -   The pickup is a general location.

Pickup points for an experience on [Musement.com][6] are separated between the two types:

![pickup division](https://porta.redoc.ly/static/b631fe1b4ac848ea08480d61a94cd585/691c3/pickup-division.png "pickup division")

## [][7]Coordinates

When creating a pickup point, you can choose to indicate its exact location by including `latitude` and `longitude` properties.

## [][8]Offsetting pickup times

When creating a pickup point, the request can also include an optional `time_margin` property to indicate how many minutes a pickup will occur before (or after) an [availability time slot][9].

## [][10]Managing pickups for a time slot

Pickups can only be used for experiences that use time slots, when the `availability_slot_type` property value is `TIME`. The pickups are not assigned directly to experiences, but rather to an [_availability slot_][11]. This allows you to set up different pickups for different dates and prices (if necessary).

When creating an [availability time slot][12], include a list of pickup IDs. In the example request below, we are creating an availability slot with one pickup point:

```bash
curl -X POST '{baseUrl}/supplier/availability/experiences/experience-123/options/option-123/slots' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "availability_slot_id": "slot-123", [...], "pickup_ids": [ "pickup-123" ], [...] }'
```

To add or remove a pickup from an availability time slot, you must update the slot with the modified `pickup_ids` property. In the example request below, all pickups are removed:

```bash
curl -X PUT '{baseUrl}/supplier/availability/experiences/experience-123/options/option-123/slots/slot-123' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ [...], "pickup_ids": [], [...] }'
```

[1]: https://porta.redoc.ly/experiences/mandatory-questions/
[2]: https://porta.redoc.ly/getting-started/#creating-a-pickup
[3]: https://porta.redoc.ly/getting-started/#pickup_id
[4]: https://porta.redoc.ly/getting-started/#name
[5]: https://porta.redoc.ly/getting-started/#type
[6]: https://www.musement.com/
[7]: https://porta.redoc.ly/getting-started/#coordinates
[8]: https://porta.redoc.ly/getting-started/#offsetting-pickup-times
[9]: https://porta.redoc.ly/experiences/availability-slots/time/
[10]: https://porta.redoc.ly/getting-started/#managing-pickups-for-a-time-slot
[11]: https://porta.redoc.ly/experiences/availability-slots/
[12]: https://porta.redoc.ly/experiences/availability-slots/time/
