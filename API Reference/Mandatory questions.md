---
created: 2024-08-06T01:11:58 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# Mandatory questions

> ## Excerpt
> Mandatory questions allow suppliers to request customer information. Experiences are not required to have mandatory questions. However, when mandatory questions are present, customers must provide answers to complete a booking.

---
Mandatory questions allow suppliers to request customer information. Experiences are not required to have mandatory questions. However, when mandatory questions are present, customers must provide answers to complete a booking.

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions)Get mandatory questions for experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=path&amp;path=experience_id&amp;t=request" id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept&amp;t=request" data-section-id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept&amp;t=request" id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept-version&amp;t=request" id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

200

Mandatory questions for experience

get/supplier/catalog/experiences/{experience\_id}/mandatory-questions

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/experiences/{experience_id}/mandatory-questions'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`[`

-   `{`
    
    -   `"data_pattern": "string",`
        
    -   `"data_type": "DATE",`
        
    -   `"holder_category_id": null,`
        
    -   `"level": "BOOKING",`
        
    -   `"mandatory_question_id": "string",`
        
    -   `"option_id": null,`
        
    -   `"question": "string",`
        
    -   `"select": {}`
        
    
    `}`
    

`]`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions)Create mandatory question for experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=path&amp;path=experience_id&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept-version&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="data_pattern"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=data_pattern&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=data_pattern&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=data_pattern&amp;t=request"></a>data_pattern</span></td><td><div><p><span></span><span>string</span></p><div><p>For unsupported data types, suppliers can provide a regular expression validation pattern. The <code>data_type</code> property must be <code>STRING</code> to use this feature.</p></div></div></td></tr><tr><td kind="field" title="data_type"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=data_type&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=data_type&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=data_type&amp;t=request"></a>data_type</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The type of data the question will collect.</p></div><div><table><thead><tr><th><span>Enum:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>DATE</td><td><span><p>Customers must select a single date.</p></span></td></tr><tr><td>DECIMAL</td><td><span><p>Customers must provide a decimal number value.</p></span></td></tr><tr><td>EMAIL</td><td><span><p>Customers must provide a valid email address.</p></span></td></tr><tr><td>INTEGER</td><td><span><p>Customers must provide an integer value.</p></span></td></tr><tr><td>PHONE_NUMBER</td><td><span><p>Customers must provide a phone number.</p></span></td></tr><tr><td>SELECT_ONE</td><td><span><p>Customers must select one value.</p></span></td></tr><tr><td>STRING</td><td><span><p>Customers must provide a text value.</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="holder_category_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=holder_category_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=holder_category_id&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=holder_category_id&amp;t=request"></a>holder_category_id</span></td><td><div><p><span></span><span>null or string</span></p><div><p>The holder category associated with the question. When <code>null</code>, the question is applied to all holder categories.</p></div></div></td></tr><tr><td kind="field" title="level"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=level&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=level&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=level&amp;t=request"></a>level</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The level determines how to request the question: once per booking or once per person in a booking.</p></div><div><table><thead><tr><th><span>Enum:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>BOOKING</td><td><span><p>The question must be answered once per booking.</p></span></td></tr><tr><td>BY_PAX</td><td><span><p>The question must be answered once per person in a booking.</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="mandatory_question_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=mandatory_question_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=mandatory_question_id&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=mandatory_question_id&amp;t=request"></a>mandatory_question_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The mandatory question ID, assigned by the supplier.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=option_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=option_id&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=option_id&amp;t=request"></a>option_id</span></td><td><div><p><span></span><span>null or string</span></p><div><p>The option associated with the question. When <code>null</code>, the question is applied to all options.</p></div></div></td></tr><tr><td kind="field" title="question"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=question&amp;t=request" data-section-id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=question&amp;t=request" id="tag/mandatory-questions/operation/post/catalog/experiences/experience_id/mandatory-questions!path=question&amp;t=request"></a>question</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The human-friendly question to show customers.</p></div></div></td></tr><tr><td kind="field" title="select"></td><td><div><p><span></span><span>object</span></p><div><p>When the <code>data_type</code> property is <code>SELECT_ONE</code>, use the <code>select</code> property to provide options for customers to select. The property value must be a key-value object of strings.</p></div></div></td></tr></tbody></table>

200

Mandatory question for experience

post/supplier/catalog/experiences/{experience\_id}/mandatory-questions

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"data_pattern": "string",`
    
-   `"data_type": "DATE",`
    
-   `"holder_category_id": null,`
    
-   `"level": "BOOKING",`
    
-   `"mandatory_question_id": "string",`
    
-   `"option_id": null,`
    
-   `"question": "string",`
    
-   `"select": {`
    
    -   `"Raw key value1": "string",`
        
    -   `"Raw key value2": "string"`
        
    
    `}`
    

`}`

-   200
-   default

`{`

-   `"data_pattern": "string",`
    
-   `"data_type": "DATE",`
    
-   `"holder_category_id": null,`
    
-   `"level": "BOOKING",`
    
-   `"mandatory_question_id": "string",`
    
-   `"option_id": null,`
    
-   `"question": "string",`
    
-   `"select": {`
    
    -   `"Raw key value1": "string",`
        
    -   `"Raw key value2": "string"`
        
    
    `}`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id)Remove mandatory question from experience

A mandatory question cannot be removed if it is part of a hold availability request.

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request" id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="mandatory_question_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request" id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request"></a>mandatory_question_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The mandatory question ID.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request" id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request" id="tag/mandatory-questions/operation/delete/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

204

Mandatory question removed successfully

delete/supplier/catalog/experiences/{experience\_id}/mandatory-questions/{mandatory\_question\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> DELETE <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/experiences/{experience_id}/mandatory-questions/{mandatory_question_id}'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   default

400 Bad request: check the request for errors

`{`

-   `"code": "400",`
    
-   `"id": "3ecae132-a32d-41f9-8f7d-586f34cc29ce",`
    
-   `"message": "Check the request for errors."`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id)Get mandatory question for experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request" id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="mandatory_question_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request" id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request"></a>mandatory_question_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The mandatory question ID.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request" id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request" id="tag/mandatory-questions/operation/get/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

200

Mandatory question for experience

get/supplier/catalog/experiences/{experience\_id}/mandatory-questions/{mandatory\_question\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/experiences/{experience_id}/mandatory-questions/{mandatory_question_id}'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`{`

-   `"data_pattern": "string",`
    
-   `"data_type": "DATE",`
    
-   `"holder_category_id": null,`
    
-   `"level": "BOOKING",`
    
-   `"mandatory_question_id": "string",`
    
-   `"option_id": null,`
    
-   `"question": "string",`
    
-   `"select": {`
    
    -   `"Raw key value1": "string",`
        
    -   `"Raw key value2": "string"`
        
    
    `}`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id)Update mandatory question for experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="mandatory_question_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=path&amp;path=mandatory_question_id&amp;t=request"></a>mandatory_question_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The mandatory question ID.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="data_pattern"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=data_pattern&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=data_pattern&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=data_pattern&amp;t=request"></a>data_pattern</span></td><td><div><p><span></span><span>string</span></p><div><p>For unsupported data types, suppliers can provide a regular expression validation pattern. The <code>data_type</code> property must be <code>STRING</code> to use this feature.</p></div></div></td></tr><tr><td kind="field" title="data_type"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=data_type&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=data_type&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=data_type&amp;t=request"></a>data_type</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The type of data the question will collect.</p></div><div><table><thead><tr><th><span>Enum:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>DATE</td><td><span><p>Customers must select a single date.</p></span></td></tr><tr><td>DECIMAL</td><td><span><p>Customers must provide a decimal number value.</p></span></td></tr><tr><td>EMAIL</td><td><span><p>Customers must provide a valid email address.</p></span></td></tr><tr><td>INTEGER</td><td><span><p>Customers must provide an integer value.</p></span></td></tr><tr><td>PHONE_NUMBER</td><td><span><p>Customers must provide a phone number.</p></span></td></tr><tr><td>SELECT_ONE</td><td><span><p>Customers must select one value.</p></span></td></tr><tr><td>STRING</td><td><span><p>Customers must provide a text value.</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="holder_category_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=holder_category_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=holder_category_id&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=holder_category_id&amp;t=request"></a>holder_category_id</span></td><td><div><p><span></span><span>null or string</span></p><div><p>The holder category associated with the question. When <code>null</code>, the question is applied to all holder categories.</p></div></div></td></tr><tr><td kind="field" title="level"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=level&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=level&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=level&amp;t=request"></a>level</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The level determines how to request the question: once per booking or once per person in a booking.</p></div><div><table><thead><tr><th><span>Enum:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>BOOKING</td><td><span><p>The question must be answered once per booking.</p></span></td></tr><tr><td>BY_PAX</td><td><span><p>The question must be answered once per person in a booking.</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="mandatory_question_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=mandatory_question_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=mandatory_question_id&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=mandatory_question_id&amp;t=request"></a>mandatory_question_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The mandatory question ID, assigned by the supplier.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=option_id&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=option_id&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=option_id&amp;t=request"></a>option_id</span></td><td><div><p><span></span><span>null or string</span></p><div><p>The option associated with the question. When <code>null</code>, the question is applied to all options.</p></div></div></td></tr><tr><td kind="field" title="question"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=question&amp;t=request" data-section-id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=question&amp;t=request" id="tag/mandatory-questions/operation/put/catalog/experiences/experience_id/mandatory-questions/mandatory_question_id!path=question&amp;t=request"></a>question</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The human-friendly question to show customers.</p></div></div></td></tr><tr><td kind="field" title="select"></td><td><div><p><span></span><span>object</span></p><div><p>When the <code>data_type</code> property is <code>SELECT_ONE</code>, use the <code>select</code> property to provide options for customers to select. The property value must be a key-value object of strings.</p></div></div></td></tr></tbody></table>

200

Mandatory question for experience

put/supplier/catalog/experiences/{experience\_id}/mandatory-questions/{mandatory\_question\_id}

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"data_pattern": "string",`
    
-   `"data_type": "DATE",`
    
-   `"holder_category_id": null,`
    
-   `"level": "BOOKING",`
    
-   `"mandatory_question_id": "string",`
    
-   `"option_id": null,`
    
-   `"question": "string",`
    
-   `"select": {`
    
    -   `"Raw key value1": "string",`
        
    -   `"Raw key value2": "string"`
        
    
    `}`
    

`}`

-   200
-   default

`{`

-   `"data_pattern": "string",`
    
-   `"data_type": "DATE",`
    
-   `"holder_category_id": null,`
    
-   `"level": "BOOKING",`
    
-   `"mandatory_question_id": "string",`
    
-   `"option_id": null,`
    
-   `"question": "string",`
    
-   `"select": {`
    
    -   `"Raw key value1": "string",`
        
    -   `"Raw key value2": "string"`
        
    
    `}`
    

`}`
