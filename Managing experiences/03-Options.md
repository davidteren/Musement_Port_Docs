---
created: 2024-07-15T22:50:07 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Options

> ## Excerpt
> Create options in PORTA to give customers something to choose for their bookings.

---
Last updated 2 months ago

Options are variations to the main experience. Customers must choose an option to complete a booking.

## [][1]Creating an option

Options can either be created when [creating an experience][2] or by using the `POST /supplier/catalog/experiences/{experience_id}/options` endpoint.

An option must contain the following properties:

### [][3]`option_id`

The option ID, assigned by the supplier.

### [][4]`label`

The human-friendly label for the option that customers will see.

### [][5]`holder_categories`

Every option must have at least one [holder category][6], the type of person making a booking.

## [][7]Limiting quantities

Suppliers can set a minimum quantity required for a booking with an option's `min_booking_quantity` property. Only bookings with a total quantity that is greater than or equal to this value are accepted.

Suppliers can set a maximum limit per booking with an option's `max_booking_quantity` property. Only bookings with a total quantity that is less than or equal to this value are accepted. When no maximum is specified, no limit is placed on the booking quantity.

## [][8]Changing the order

While PORTA returns options sorted by the order they were created, on [musement.com][9] options appear in order from **least to most expensive**. Suppliers can modify this order by assigning a `main_option` property value of `true` to a single option. The main option for an experience will appear first in the list of options on [musement.com][10]:

![options](https://porta.redoc.ly/static/4e0cb07935ee7c2aee970f76982feb82/a805e/options.png "options")

[1]: https://porta.redoc.ly/getting-started/#creating-an-option
[2]: https://porta.redoc.ly/experiences/
[3]: https://porta.redoc.ly/getting-started/#option_id
[4]: https://porta.redoc.ly/getting-started/#label
[5]: https://porta.redoc.ly/getting-started/#holder_categories
[6]: https://porta.redoc.ly/experiences/holder-categories/
[7]: https://porta.redoc.ly/getting-started/#limiting-quantities
[8]: https://porta.redoc.ly/getting-started/#changing-the-order
[9]: http://www.musement.com/
[10]: http://www.musement.com/
