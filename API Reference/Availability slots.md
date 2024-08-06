---
created: 2024-08-06T01:12:28 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# Availability slots

> ## Excerpt
> Availability slots is the term for any type of slot used for a booking. This collection of endpoints will work for any type of slot

---
Availability slots is the term for any type of slot used for a booking. This collection of endpoints will work for any type of slot

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots)Remove availability slots from option

An availability slot cannot be deleted if it is part of a hold availability request.

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=experience_id&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=option_id&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept-version&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="API-Key"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=API-Key&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=API-Key&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=API-Key&amp;t=request"></a>API-Key</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (API key) </span><span>^[a-zA-Z0-9-_\.]{3,50}$</span></p><div><p>The supplier's API key</p></div></div></td></tr></tbody></table>

204

Availability slots removed successfully from option

delete/supplier/availability/experiences/{experience\_id}/options/{option\_id}/slots

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> DELETE <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/availability/experiences/{experience_id}/options/{option_id}/slots'</span> <span>\</span>
  <span>-H</span> <span>'API-Key: string'</span> <span>\</span>
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

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots)Create availability slots for experience

The maximum number of items in the request body varies based on the type of availability slot:

-   Daily slot: 100
-   Open slot: 1
-   Time slot: 100

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=experience_id&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=option_id&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept-version&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="API-Key"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=API-Key&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=API-Key&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!in=header&amp;path=API-Key&amp;t=request"></a>API-Key</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (API key) </span><span>^[a-zA-Z0-9-_\.]{3,50}$</span></p><div><p>The supplier's API key</p></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

Array

<table><tbody><tr><td kind="field" title="capacity"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/capacity&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/capacity&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/capacity&amp;t=request"></a>capacity</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><div><p>The remaining number of seats for the slot.</p></div></div></td></tr><tr><td kind="field" title="daily_slot"><p>required</p></td><td><div><p><span></span><span>object</span><span> (Daily slot)</span></p></div></td></tr><tr><td kind="field" title="available_holder_categories"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> (Holder categories) </span><span><span>unique</span></span></p><div><p>Holder categories for the slot.</p></div></div></td></tr><tr><td kind="field" title="guide_languages"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/guide_languages&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/guide_languages&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/guide_languages&amp;t=request"></a>guide_languages</span></td><td><div><p><span>Array of </span><span>strings</span><span> (Languages) </span><span><span>unique</span></span></p><div><p>A list of languages which can be booked for the slot. The languages will appear for <em>all</em> available holder categories in the slot.</p><p>This property must follow the <a href="https://www.iso.org/iso-639-language-codes.html">ISO 639-1 standard</a>.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/option_id&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/option_id&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID of the option that the slot belongs to.</p></div></div></td></tr><tr><td kind="field" title="slot_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/slot_id&amp;t=request" data-section-id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/slot_id&amp;t=request" id="tag/availability-slots/operation/post/availability/experiences/experience_id/options/option_id/slots!path=0/slot_id&amp;t=request"></a>slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The availability slot ID, assigned by the supplier.</p><p>The ID must be unique. The same ID cannot be re-used for different experiences.</p></div></div></td></tr></tbody></table>

post/supplier/availability/experiences/{experience\_id}/options/{option\_id}/slots

-   Payload
-   curl
-   C#
-   Node.js

`[`

-   `{`
    
    -   `"capacity": 0,`
        
    -   `"daily_slot": {},`
        
    -   `"available_holder_categories": [],`
        
    -   `"guide_languages": [],`
        
    -   `"option_id": "string",`
        
    -   `"slot_id": "string"`
        
    
    `}`
    

`]`

-   200
-   default

`{`

-   `"capacity": 0,`
    
-   `"daily_slot": {`
    
    -   `"date": "2019-08-24"`
        
    
    `},`
    
-   `"available_holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"guide_languages": [`
    
    -   `"string"`
        
    
    `],`
    
-   `"option_id": "string",`
    
-   `"slot_id": "string"`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id)Remove availability slot from option

An availability slot cannot be deleted if it is part of a hold availability request.

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="availability_slot_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request"></a>availability_slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The availability slot ID.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" id="tag/availability-slots/operation/delete/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

204

Availability slot removed successfully from option

delete/supplier/availability/experiences/{experience\_id}/options/{option\_id}/slots/{availability\_slot\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> DELETE <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/availability/experiences/{experience_id}/options/{option_id}/slots/{availability_slot_id}'</span> <span>\</span>
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

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id)Get availability slot for option

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="availability_slot_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" data-section-id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request"></a>availability_slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The availability slot ID.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" id="tag/availability-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

get/supplier/availability/experiences/{experience\_id}/options/{option\_id}/slots/{availability\_slot\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/availability/experiences/{experience_id}/options/{option_id}/slots/{availability_slot_id}'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`{`

-   `"capacity": 0,`
    
-   `"daily_slot": {`
    
    -   `"date": "2019-08-24"`
        
    
    `},`
    
-   `"available_holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"guide_languages": [`
    
    -   `"string"`
        
    
    `],`
    
-   `"option_id": "string",`
    
-   `"slot_id": "string"`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id)Update capacity for availability slot

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="availability_slot_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" data-section-id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request"></a>availability_slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The availability slot ID.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="capacity"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=capacity&amp;t=request" data-section-id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=capacity&amp;t=request" id="tag/availability-slots/operation/patch/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=capacity&amp;t=request"></a>capacity</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><div><p>The remaining number of seats for the slot.</p></div></div></td></tr></tbody></table>

patch/supplier/availability/experiences/{experience\_id}/options/{option\_id}/slots/{availability\_slot\_id}

-   Payload
-   curl
-   C#
-   Node.js

-   200
-   default

`{`

-   `"capacity": 0,`
    
-   `"daily_slot": {`
    
    -   `"date": "2019-08-24"`
        
    
    `},`
    
-   `"available_holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"guide_languages": [`
    
    -   `"string"`
        
    
    `],`
    
-   `"option_id": "string",`
    
-   `"slot_id": "string"`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id)Update availability slot for option

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="availability_slot_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=path&amp;path=availability_slot_id&amp;t=request"></a>availability_slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The availability slot ID.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="capacity"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/capacity&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/capacity&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/capacity&amp;t=request"></a>capacity</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><div><p>The remaining number of seats for the slot.</p></div></div></td></tr><tr><td kind="field" title="daily_slot"><p>required</p></td><td><div><p><span></span><span>object</span><span> (Daily slot)</span></p></div></td></tr><tr><td kind="field" title="available_holder_categories"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> (Holder categories) </span><span><span>unique</span></span></p><div><p>Holder categories for the slot.</p></div></div></td></tr><tr><td kind="field" title="guide_languages"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/guide_languages&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/guide_languages&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/guide_languages&amp;t=request"></a>guide_languages</span></td><td><div><p><span>Array of </span><span>strings</span><span> (Languages) </span><span><span>unique</span></span></p><div><p>A list of languages which can be booked for the slot. The languages will appear for <em>all</em> available holder categories in the slot.</p><p>This property must follow the <a href="https://www.iso.org/iso-639-language-codes.html">ISO 639-1 standard</a>.</p></div></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/option_id&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/option_id&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID of the option that the slot belongs to.</p></div></div></td></tr><tr><td kind="field" title="slot_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/slot_id&amp;t=request" data-section-id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/slot_id&amp;t=request" id="tag/availability-slots/operation/put/availability/experiences/experience_id/options/option_id/slots/availability_slot_id!path=0/slot_id&amp;t=request"></a>slot_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The availability slot ID, assigned by the supplier.</p><p>The ID must be unique. The same ID cannot be re-used for different experiences.</p></div></div></td></tr></tbody></table>

put/supplier/availability/experiences/{experience\_id}/options/{option\_id}/slots/{availability\_slot\_id}

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"capacity": 0,`
    
-   `"daily_slot": {`
    
    -   `"date": "2019-08-24"`
        
    
    `},`
    
-   `"available_holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"guide_languages": [`
    
    -   `"string"`
        
    
    `],`
    
-   `"option_id": "string",`
    
-   `"slot_id": "string"`
    

`}`

-   200
-   default

`{`

-   `"capacity": 0,`
    
-   `"daily_slot": {`
    
    -   `"date": "2019-08-24"`
        
    
    `},`
    
-   `"available_holder_categories": [`
    
    -   `{}`
        
    
    `],`
    
-   `"guide_languages": [`
    
    -   `"string"`
        
    
    `],`
    
-   `"option_id": "string",`
    
-   `"slot_id": "string"`
    

`}`
