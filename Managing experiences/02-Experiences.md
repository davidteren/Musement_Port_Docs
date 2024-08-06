---
created: 2024-07-15T22:50:03 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Experiences

> ## Excerpt
> Use PORTA to create experiences for Musement's distribution platforms.

---
Last updated 2 months ago

Experiences can be almost anything: tickets for museums, wine tastings, tours, etc. They are the core of the Musement catalog.

## [][1]Creating an experience

When creating an experience in PORTA, suppliers must use the `POST /supplier/catalog/experiences` endpoint:

```bash
curl '{baseUrl}/supplier/catalog/experiences' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "availability_slot_type": "TIME", "currency": "USD", "cutoff_time": "P1D", "experience_id": "abc-123", "experience_name": "Example tour with attraction tickets", "external_experience_id": "Example-123", "external_experience_name": "Example tour and admission", "options": [], "vendor_id": "vendor-123" }'
```

The following information is required for the request:

### [][2]`availability_slot_type`

This property determines how customers will book the experience. It accepts the following values:

-   `DAILY`
    -   Customers must select a date for their booking. They do not select a time.
-   `OPEN`
    -   Customers do not select a date or time. Their booking expires on a set date or a set number of days after purchase.
-   `TIME`
    -   Customers must select a date and time for their booking.

### [][3]`currency`

The currency used for billing. The value must follow the [ISO 4217 standard][4].

### [][5]`experience_id`

Suppliers must provide their own ID for the experience. This ID will be used for all related API requests.

### [][6]`experience_name`

Give the experience a name to make it easier to recognize whenever you access PORTA.

### [][7]`options`

A list of bookable options for the experience. An experience must have [at least one option][8] to start with. Options can be added and removed later.

### [][9]`vendor_id`

The experience's [vendor][10].

## [][11]Setting a cutoff time

When creating an experience, you can specify a `cutoff_time` value. This is the minimum amount of time required to book a travel date in advance.

The value must follow the [ISO 8601 standard][12].

## [][13]External values

If the names and IDs of experiences vary differently between PORTA and your system, there are two optional properties you can use to help keep track of your products:

-   `external_experience_id`
    -   The ID of the experience as it appears in your own system.
-   `external_experience_name`
    -   The name of the experience as it appears in your own system.

## [][14]Archiving an experience

The `archived` property determines whether an experience is for sale or not. By default, new experiences are not archived. When an experience is archived, its corresponding activity in the business platform (if any) is also archived to stop sales.

Archiving is an acceptable approach to closing experiences that will never be available again. Suppliers may also choose to archive experiences temporarily. However, be aware that once an activity is archived, suppliers need the help of the _Content Supplier Connectivity_ team to un-archive the business platform activity.

##### Time to archive

When an experience is archived, it may take up to 24 hours for Musement websites to update. To avoid receiving further bookings, we encourage suppliers to archive the corresponding business platform activity too.

## [][15]Updating an experience

Suppliers can update a selection of experience properties with the `PATCH /supplier/catalog/experiences/{experience_id}` endpoint:

```bash
curl '{baseUrl}/supplier/catalog/experiences/abc-123' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "archived": true, "cutoff_time": "P3D", "experience_name": "Example tour with attraction tickets and lunch", "external_experience_id": "Example-123-lunch", "external_experience_name": "Example tour and admission with lunch", "vendor_id": "vendor-123-lunch" }'
```

Suppliers can choose to update one or more properties with this endpoint.

Changes may take up to 24 hours to appear on the business platform and Musement distribution websites.

[1]: https://porta.redoc.ly/getting-started/#creating-an-experience
[2]: https://porta.redoc.ly/getting-started/#availability_slot_type
[3]: https://porta.redoc.ly/getting-started/#currency
[4]: https://www.iso.org/iso-4217-currency-codes.html
[5]: https://porta.redoc.ly/getting-started/#experience_id
[6]: https://porta.redoc.ly/getting-started/#experience_name
[7]: https://porta.redoc.ly/getting-started/#options
[8]: https://porta.redoc.ly/experiences/options/
[9]: https://porta.redoc.ly/getting-started/#vendor_id
[10]: https://porta.redoc.ly/experiences/vendors/
[11]: https://porta.redoc.ly/getting-started/#setting-a-cutoff-time
[12]: https://www.iso.org/iso-8601-date-and-time-format.html
[13]: https://porta.redoc.ly/getting-started/#external-values
[14]: https://porta.redoc.ly/getting-started/#archiving-an-experience
[15]: https://porta.redoc.ly/getting-started/#updating-an-experience
