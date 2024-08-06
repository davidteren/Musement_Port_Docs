---
created: 2024-07-15T22:50:12 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Holder categories

> ## Excerpt
> Use holder categories in PORTA so that customers can select the type of person for a booking.

---
Last updated 2 months ago

Holder categories are part of [options][1]. They describe the type of person for a booking.

## [][2]Creating a holder category

Holder categories do not have their own endpoint. They are part of an [option][3].

Each holder category in an option must have the follow properties:

### [][4]`holder_category_id`

The supplier's ID for the holder category.

### [][5]`holder_type`

The type of holder category. This value affects how the holder category appears on Musement. Choices are limited to:

-   `ADULT`
-   `CHILD`
-   `FAMILY`
-   `GROUP`
-   `INFANT`
-   `MILITARY`
-   `REGULAR`
-   `SENIOR`
-   `STUDENT`
-   `YOUTH`

An additional `CUSTOM*` value is available but requires approval with the _Integrations_ team before usage.

### [][6]`minimum_age`

The minimum age a customer must have to qualify for this holder category.

While not required, there is a `maximum_age` property which can be used to specify the maximum age a customer can have to qualify for a holder category.

## [][7]Changing the order

While PORTA returns holder categories sorted by the order they were created, on [musement.com][8] holder categories appear in order from **most to least expensive**. Suppliers can modify this order by assigning a `default_category` property value of `true` to a single holder category in an option. The main holder category for an experience will appear first in the list of holder categories on [musement.com][9]:

![holders](https://porta.redoc.ly/static/e9248d9b38c99305b3b317e22e134aa2/76aed/holders.png "holders")

[1]: https://porta.redoc.ly/experiences/options/
[2]: https://porta.redoc.ly/getting-started/#creating-a-holder-category
[3]: https://porta.redoc.ly/experiences/options/
[4]: https://porta.redoc.ly/getting-started/#holder_category_id
[5]: https://porta.redoc.ly/getting-started/#holder_type
[6]: https://porta.redoc.ly/getting-started/#minimum_age
[7]: https://porta.redoc.ly/getting-started/#changing-the-order
[8]: http://www.musement.com/
[9]: http://www.musement.com/
