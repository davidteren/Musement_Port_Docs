---
created: 2024-08-06T01:12:09 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# Options

> ## Excerpt
> Options are a variations of an experience. A customer must select an option to complete a booking.

---
Options are a variations of an experience. A customer must select an option to complete a booking.

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options)Create option for experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!in=path&amp;path=experience_id&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!in=header&amp;path=accept&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!in=header&amp;path=accept&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!in=header&amp;path=accept-version&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="holder_categories"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> (Holder category) </span><span><span>unique</span></span></p><div><p>The holder categories for the option.</p></div></div></td></tr><tr><td kind="field" title="label"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!path=label&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!path=label&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!path=label&amp;t=request"></a>label</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The human-friendly label for the option.</p></div></div></td></tr><tr><td kind="field" title="main_option"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!path=main_option&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!path=main_option&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!path=main_option&amp;t=request"></a>main_option</span></td><td><div><p><span></span><span>boolean</span></p><div><p>When <code>true</code>, the main option appears first in the list of options.</p><p>If no option is defined as the default, then the first option is automatically made the default.</p></div></div></td></tr><tr><td kind="field" title="max_booking_quantity"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!path=max_booking_quantity&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!path=max_booking_quantity&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!path=max_booking_quantity&amp;t=request"></a>max_booking_quantity</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><div><p>The maximum quantity allowed per booking.</p></div></div></td></tr><tr><td kind="field" title="min_booking_quantity"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!path=min_booking_quantity&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!path=min_booking_quantity&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!path=min_booking_quantity&amp;t=request"></a>min_booking_quantity</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><div><p>The minimum quantity required for a valid booking.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/post/catalog/experiences/experience_id/options!path=option_id&amp;t=request" data-section-id="tag/options/operation/post/catalog/experiences/experience_id/options!path=option_id&amp;t=request" id="tag/options/operation/post/catalog/experiences/experience_id/options!path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The option ID, assigned by the supplier.</p></div></div></td></tr></tbody></table>

post/supplier/catalog/experiences/{experience\_id}/options

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"label": "string",`
    
-   `"main_option": true,`
    
-   `"max_booking_quantity": 0,`
    
-   `"min_booking_quantity": 0,`
    
-   `"option_id": "string"`
    

`}`

-   200
-   default

`{`

-   `"holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"label": "string",`
    
-   `"main_option": true,`
    
-   `"max_booking_quantity": 0,`
    
-   `"min_booking_quantity": 0,`
    
-   `"option_id": "string"`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/delete/catalog/experiences/experience_id/options/option_id)Remove option from experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=path&amp;path=experience_id&amp;t=request" id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=path&amp;path=option_id&amp;t=request" id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept&amp;t=request" id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept-version&amp;t=request" id="tag/options/operation/delete/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

204

Option removed successfully

delete/supplier/catalog/experiences/{experience\_id}/options/{option\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> DELETE <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/experiences/{experience_id}/options/{option_id}'</span> <span>\</span>
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

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id)Update option for experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=path&amp;path=experience_id&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=path&amp;path=option_id&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept-version&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="holder_categories"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> (Holder category) </span><span><span>unique</span></span></p><div><p>The holder categories for the option.</p></div></div></td></tr><tr><td kind="field" title="label"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=label&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=label&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=label&amp;t=request"></a>label</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The human-friendly label for the option.</p></div></div></td></tr><tr><td kind="field" title="main_option"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=main_option&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=main_option&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=main_option&amp;t=request"></a>main_option</span></td><td><div><p><span></span><span>boolean</span></p><div><p>When <code>true</code>, the main option appears first in the list of options.</p><p>If no option is defined as the default, then the first option is automatically made the default.</p></div></div></td></tr><tr><td kind="field" title="max_booking_quantity"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=max_booking_quantity&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=max_booking_quantity&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=max_booking_quantity&amp;t=request"></a>max_booking_quantity</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><div><p>The maximum quantity allowed per booking.</p></div></div></td></tr><tr><td kind="field" title="min_booking_quantity"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=min_booking_quantity&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=min_booking_quantity&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=min_booking_quantity&amp;t=request"></a>min_booking_quantity</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><div><p>The minimum quantity required for a valid booking.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=option_id&amp;t=request" data-section-id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=option_id&amp;t=request" id="tag/options/operation/put/catalog/experiences/experience_id/options/option_id!path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The option ID, assigned by the supplier.</p></div></div></td></tr></tbody></table>

409

Conflict: request conflicts with target resource

put/supplier/catalog/experiences/{experience\_id}/options/{option\_id}

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"label": "string",`
    
-   `"main_option": true,`
    
-   `"max_booking_quantity": 0,`
    
-   `"min_booking_quantity": 0,`
    
-   `"option_id": "string"`
    

`}`

-   200
-   409
-   default

`{`

-   `"holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"label": "string",`
    
-   `"main_option": true,`
    
-   `"max_booking_quantity": 0,`
    
-   `"min_booking_quantity": 0,`
    
-   `"option_id": "string"`
    

`}`
