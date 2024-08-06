---
created: 2024-07-15T22:50:52 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Mandatory questions

> ## Excerpt
> Mandatory questions allow PORTA to collect customer information that you need to complete booking.

---
Last updated 2 months ago

Mandatory questions allow suppliers to request customer information. Experiences are not required to have mandatory questions. However, when mandatory questions are present, customers must provide answers to complete a booking.

## [][1]Creating a mandatory question

Suppliers must use the `POST /supplier/catalog/experience/{experience_id}/mandatory-questions` endpoint to create a mandatory question for an experience:

```bash
curl -X POST '{baseUrl}/supplier/catalog/experience/experience-123/mandatory-questions' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "data_type": "string", "level": "BY_PAX", "mandatory_question_id": "question-123", "question": "What is your favorite color?" }'
```

When creating a mandatory question, the request must contain the following properties:

### [][2]`data_type`

The type of data you are collecting. Based on the value of this property, the resulting field appearance will change on the Musement platform and additional validation checks may take place.

Currently, the following values are valid:

-   `DATE`
    -   Customers must select a single date.
-   `DECIMAL`
    -   Customers must provide a decimal number value.
-   `EMAIL`
    -   Customers must provide a valid email address.
-   `INTEGER`
    -   Customers must provide an integer value.
-   `PHONE_NUMBER`
    -   Customers must provide a phone number.
-   `SELECT_ONE`
    -   Customers must select one value.
-   `STRING`
    -   Customers must provide a text value.

### [][3]`level`

The `level` property determines whether the question is presented once per booking or once per person in a booking:

-   `BOOKING` : The question is presented once per booking.
-   `BY_PAX` : The question is presented once per person in a booking.

### [][4]`mandatory_question_id`

Suppliers must provide their own ID for the mandatory question.

### [][5]`question`

The human-friendly question to show customers in English.

## [][6]Assigning questions to options and holder categories

By default, a mandatory question is applied to all options and holder categories in an experience.

You can restrict a question to specific options and holder categories by passing their `option_id` and `holder_category_id` in the request.

In the example request below, we are updating a question to a child holder category (ID `category-child-123`):

```bash
curl -X PUT '{baseUrl}/supplier/catalog/experience/experience-123/mandatory-questions/question-123' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "data_type": "STRING", "holder_category_id": "category-child-123", "level": "BY_PAX", "mandatory_question_id": "question-123", "question": "What is your favorite color?" }'
```

You can limit a mandatory question to both an option and holder category too:

```bash
curl -X PUT '{baseUrl}/supplier/catalog/experience/experience-123/mandatory-questions/question-123' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "data_type": "STRING", "holder_category_id": "category-child-123", "level": "BY_PAX", "mandatory_question_id": "question-123", "option_id": "option-123", "question": "What is your favorite color?" }'
```

## [][7]Giving customers options

When a mandatory question's `data_type` property is `SELECT_ONE`, customers are offered a list of options to choose from.

Suppliers must use add the `select` property to define the options to list. The property value must contain string key-value pairs, with the raw value and human-friendly version.

In the example request below, customers must select between two choices:

```bash
curl -X PUT '{baseUrl}/supplier/catalog/experience/experience-123/mandatory-questions/question-123' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "data_type": "SELECT_ONE", "holder_category_id": "category-child-123", "level": "BY_PAX", "mandatory_question_id": "question-123", "question": "What is your favorite color?", "select": { "red": "Red", "blue": "No, blue!" } }'
```

## [][8]Other data types

If you require the responses to mandatory questions to conform to a particular pattern, you can use the `data_pattern` property to define a regular expression that will be used for validation.

This property can only be used when the `data_type` property value is `STRING`.

In the example response below, we are creating a mandatory question which only accepts lowercase letters:

```bash
curl -X POST '{baseUrl}/supplier/catalog/experience/experience-123/mandatory-questions' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer {accessToken}' \ -H 'Content-Type: application/json' \ --data-raw '{ "data_pattern": "^[a-z]$", "data_type": "STRING", "level": "BY_PAX", "mandatory_question_id": "question-123", "question": "What is your favorite color?" }'
```

[1]: https://porta.redoc.ly/getting-started/#creating-a-mandatory-question
[2]: https://porta.redoc.ly/getting-started/#data_type
[3]: https://porta.redoc.ly/getting-started/#level
[4]: https://porta.redoc.ly/getting-started/#mandatory_question_id
[5]: https://porta.redoc.ly/getting-started/#question
[6]: https://porta.redoc.ly/getting-started/#assigning-questions-to-options-and-holder-categories
[7]: https://porta.redoc.ly/getting-started/#giving-customers-options
[8]: https://porta.redoc.ly/getting-started/#other-data-types
