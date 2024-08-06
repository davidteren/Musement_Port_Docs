---
created: 2024-08-06T01:12:20 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# Pickups

> ## Excerpt
> Pickups are locations where customers can be picked up for their experience. Experiences are not required to have pickups. However, when pickups are assigned to experience options, selecting a pickup is required to complete a booking.

---
Pickups are locations where customers can be picked up for their experience. Experiences are not required to have pickups. However, when pickups are assigned to experience options, selecting a pickup is required to complete a booking.

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/get/catalog/pickups)Get pickups

Security**Supplier-production** or **Supplier-sandbox**

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/get/catalog/pickups!in=header&amp;path=accept&amp;t=request" data-section-id="tag/pickups/operation/get/catalog/pickups!in=header&amp;path=accept&amp;t=request" id="tag/pickups/operation/get/catalog/pickups!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/get/catalog/pickups!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/pickups/operation/get/catalog/pickups!in=header&amp;path=accept-version&amp;t=request" id="tag/pickups/operation/get/catalog/pickups!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

get/supplier/catalog/pickups

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  https://prod.api.tui/tui-musement-porta/supplier/catalog/pickups <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`[`

-   `{`
    
    -   `"name": "string",`
        
    -   `"type": "HOTEL",`
        
    -   `"latitude": -90,`
        
    -   `"longitude": -180,`
        
    -   `"pickup_id": "string",`
        
    -   `"time_margin": 0`
        
    
    `}`
    

`]`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups)Create pickup

Security**Supplier-production** or **Supplier-sandbox**

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!in=header&amp;path=accept&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!in=header&amp;path=accept&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!in=header&amp;path=accept-version&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="name"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!path=name&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!path=name&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!path=name&amp;t=request"></a>name</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The human-friendly name for the pickup.</p></div></div></td></tr><tr><td kind="field" title="type"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!path=type&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!path=type&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!path=type&amp;t=request"></a>type</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The type of pickup.</p></div><div><table><thead><tr><th><span>Enum:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>HOTEL</td><td><span><p>The pickup is at a hotel.</p></span></td></tr><tr><td>MEETING_POINT</td><td><span><p>The pickup is a general location.</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="latitude"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!path=latitude&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!path=latitude&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!path=latitude&amp;t=request"></a>latitude</span></td><td><div><p><span></span><span>number</span><span> &lt;float&gt; </span><span><span>[ -90 .. 90 ]</span></span></p><div><p>The latitude value for the pickup location. This value may be omitted.</p></div></div></td></tr><tr><td kind="field" title="longitude"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!path=longitude&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!path=longitude&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!path=longitude&amp;t=request"></a>longitude</span></td><td><div><p><span></span><span>number</span><span> &lt;float&gt; </span><span><span>[ -180 .. 180 ]</span></span></p><div><p>The longitude value for the pickup location. This value may be omitted.</p></div></div></td></tr><tr><td kind="field" title="pickup_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!path=pickup_id&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!path=pickup_id&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!path=pickup_id&amp;t=request"></a>pickup_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The pickup ID, assigned by the supplier.</p></div></div></td></tr><tr><td kind="field" title="time_margin"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/post/catalog/pickups!path=time_margin&amp;t=request" data-section-id="tag/pickups/operation/post/catalog/pickups!path=time_margin&amp;t=request" id="tag/pickups/operation/post/catalog/pickups!path=time_margin&amp;t=request"></a>time_margin</span></td><td><div><p><span></span><span>integer</span><span> &lt;int32&gt;</span></p><p><span>Default: </span><span>0</span></p><div><p>The number of minutes a pickup will occur before or after a time slot. This property accepts both positive and negative values.</p><p>A negative value indicates the pickup arrives <em>before</em> the time slot.</p><p>A positive value indicates the pickup arrives <em>after</em> the time slot.</p></div></div></td></tr></tbody></table>

post/supplier/catalog/pickups

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"name": "string",`
    
-   `"type": "HOTEL",`
    
-   `"latitude": -90,`
    
-   `"longitude": -180,`
    
-   `"pickup_id": "string",`
    
-   `"time_margin": 0`
    

`}`

-   200
-   default

`{`

-   `"name": "string",`
    
-   `"type": "HOTEL",`
    
-   `"latitude": -90,`
    
-   `"longitude": -180,`
    
-   `"pickup_id": "string",`
    
-   `"time_margin": 0`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/delete/catalog/pickups/pickup_id)Remove pickup

A pickup point cannot be removed if it is part of an availability slot. Suppliers must remove the pickup point from all availability slots first.

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="pickup_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/delete/catalog/pickups/pickup_id!in=path&amp;path=pickup_id&amp;t=request" data-section-id="tag/pickups/operation/delete/catalog/pickups/pickup_id!in=path&amp;path=pickup_id&amp;t=request" id="tag/pickups/operation/delete/catalog/pickups/pickup_id!in=path&amp;path=pickup_id&amp;t=request"></a>pickup_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/delete/catalog/pickups/pickup_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/pickups/operation/delete/catalog/pickups/pickup_id!in=header&amp;path=accept&amp;t=request" id="tag/pickups/operation/delete/catalog/pickups/pickup_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/delete/catalog/pickups/pickup_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/pickups/operation/delete/catalog/pickups/pickup_id!in=header&amp;path=accept-version&amp;t=request" id="tag/pickups/operation/delete/catalog/pickups/pickup_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

204

Pickup removed successfully

delete/supplier/catalog/pickups/{pickup\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> DELETE <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/pickups/{pickup_id}'</span> <span>\</span>
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

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/get/catalog/pickups/pickup_id)Get pickup

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="pickup_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/get/catalog/pickups/pickup_id!in=path&amp;path=pickup_id&amp;t=request" data-section-id="tag/pickups/operation/get/catalog/pickups/pickup_id!in=path&amp;path=pickup_id&amp;t=request" id="tag/pickups/operation/get/catalog/pickups/pickup_id!in=path&amp;path=pickup_id&amp;t=request"></a>pickup_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/get/catalog/pickups/pickup_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/pickups/operation/get/catalog/pickups/pickup_id!in=header&amp;path=accept&amp;t=request" id="tag/pickups/operation/get/catalog/pickups/pickup_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/pickups/operation/get/catalog/pickups/pickup_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/pickups/operation/get/catalog/pickups/pickup_id!in=header&amp;path=accept-version&amp;t=request" id="tag/pickups/operation/get/catalog/pickups/pickup_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

get/supplier/catalog/pickups/{pickup\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/pickups/{pickup_id}'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`{`

-   `"name": "string",`
    
-   `"type": "HOTEL",`
    
-   `"latitude": -90,`
    
-   `"longitude": -180,`
    
-   `"pickup_id": "string",`
    
-   `"time_margin": 0`
    

`}`
