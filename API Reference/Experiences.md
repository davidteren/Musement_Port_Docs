---
created: 2024-08-06T01:11:49 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# Experiences

> ## Excerpt
> Experiences are the products that the supplier provides. PORTA experiences can eventually be imported into Musement.

---
Experiences are the products that the supplier provides. PORTA experiences can eventually be imported into Musement.

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences)Get experiences

Security**Supplier-production** or **Supplier-sandbox**

##### query Parameters

<table><tbody><tr><td kind="field" title="vendor_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences!in=query&amp;path=vendor_id&amp;t=request" data-section-id="tag/experiences/operation/get/catalog/experiences!in=query&amp;path=vendor_id&amp;t=request" id="tag/experiences/operation/get/catalog/experiences!in=query&amp;path=vendor_id&amp;t=request"></a>vendor_id</span></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>Filter results to those which belong to the specified vendor.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences!in=header&amp;path=accept&amp;t=request" data-section-id="tag/experiences/operation/get/catalog/experiences!in=header&amp;path=accept&amp;t=request" id="tag/experiences/operation/get/catalog/experiences!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/experiences/operation/get/catalog/experiences!in=header&amp;path=accept-version&amp;t=request" id="tag/experiences/operation/get/catalog/experiences!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

get/supplier/catalog/experiences

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/experiences?vendor_id=string'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`[`

-   `{`
    
    -   `"archived": false,`
        
    -   `"availability_slot_type": "DAILY",`
        
    -   `"currency": "string",`
        
    -   `"cutoff_time": "P0D",`
        
    -   `"experience_id": "string",`
        
    -   `"experience_name": "string",`
        
    -   `"external_experience_id": "string",`
        
    -   `"external_experience_name": "string",`
        
    -   `"options": [],`
        
    -   `"vendor_id": "string"`
        
    
    `}`
    

`]`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences)Create experience

Security**Supplier-production** or **Supplier-sandbox**

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!in=header&amp;path=accept&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!in=header&amp;path=accept&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!in=header&amp;path=accept-version&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="archived"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=archived&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=archived&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=archived&amp;t=request"></a>archived</span></td><td><div><p><span></span><span>boolean</span></p><p><span>Default: </span><span>false</span></p><div><p>When an experience is archived, it is no longer for sale in Musement sites.</p><p>When an experience is un-archived, a member of the <em>Content Supplier Connectivity</em> team is required to un-archive the corresponding business platform activity.</p></div></div></td></tr><tr><td kind="field" title="availability_slot_type"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=availability_slot_type&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=availability_slot_type&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=availability_slot_type&amp;t=request"></a>availability_slot_type</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The type of availability slot for the experience.</p></div><div><table><thead><tr><th><span>Enum:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>DAILY</td><td><span><p>Customers must select a date for their booking. They do not select a time.</p></span></td></tr><tr><td>OPEN</td><td><span><p>Customers do not select a date or time. Their booking expires on a set date or a set number of days after purchase.</p></span></td></tr><tr><td>TIME</td><td><span><p>Customers must select a date and time for their booking.</p></span></td></tr></tbody></table></div></div></td></tr><tr><td kind="field" title="currency"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=currency&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=currency&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=currency&amp;t=request"></a>currency</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;currency&gt;</span></p><div><p>The currency to use for billing.</p><p>This property must follow the <a href="https://www.iso.org/iso-4217-currency-codes.html">ISO 4217 standard</a>.</p></div></div></td></tr><tr><td kind="field" title="cutoff_time"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=cutoff_time&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=cutoff_time&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=cutoff_time&amp;t=request"></a>cutoff_time</span></td><td><div><p><span></span><span>string</span><span> &lt;duration&gt;</span></p><p><span>Default: </span><span>"P0D"</span></p><div><p>The minimum amount of time required to book a travel date in advance.</p><p>This property must follow the <a href="https://www.iso.org/iso-8601-date-and-time-format.html">ISO 8601 standard</a>.</p></div></div></td></tr><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=experience_id&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=experience_id&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The experience ID, assigned by the supplier.</p></div></div></td></tr><tr><td kind="field" title="experience_name"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=experience_name&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=experience_name&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=experience_name&amp;t=request"></a>experience_name</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The name of the experience as it will appear in PORTA.</p></div></div></td></tr><tr><td kind="field" title="external_experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=external_experience_id&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=external_experience_id&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=external_experience_id&amp;t=request"></a>external_experience_id</span></td><td><div><p><span></span><span>string</span></p><div><p>An additional ID for the experience which suppliers can use for their own records.</p></div></div></td></tr><tr><td kind="field" title="external_experience_name"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=external_experience_name&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=external_experience_name&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=external_experience_name&amp;t=request"></a>external_experience_name</span></td><td><div><p><span></span><span>string</span></p><div><p>An additional name for the experience which suppliers can use for their own records.</p></div></div></td></tr><tr><td kind="field" title="options"><p>required</p></td><td><div><p><span>Array of </span><span>objects</span><span> (Options) </span><span><span>unique</span></span></p><div><p>The bookable options for the experience. This property must contain at least one option.</p></div></div></td></tr><tr><td kind="field" title="vendor_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/post/catalog/experiences!path=vendor_id&amp;t=request" data-section-id="tag/experiences/operation/post/catalog/experiences!path=vendor_id&amp;t=request" id="tag/experiences/operation/post/catalog/experiences!path=vendor_id&amp;t=request"></a>vendor_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID of the vendor that the experience belongs to.</p></div></div></td></tr></tbody></table>

post/supplier/catalog/experiences

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"archived": false,`
    
-   `"availability_slot_type": "DAILY",`
    
-   `"currency": "string",`
    
-   `"cutoff_time": "P0D",`
    
-   `"experience_id": "string",`
    
-   `"experience_name": "string",`
    
-   `"external_experience_id": "string",`
    
-   `"external_experience_name": "string",`
    
-   `"options": [`
    
    -   `{}`
        
    
    `],`
    
-   `"vendor_id": "string"`
    

`}`

-   200
-   default

`{`

-   `"archived": false,`
    
-   `"availability_slot_type": "DAILY",`
    
-   `"currency": "string",`
    
-   `"cutoff_time": "P0D",`
    
-   `"experience_id": "string",`
    
-   `"experience_name": "string",`
    
-   `"external_experience_id": "string",`
    
-   `"external_experience_name": "string",`
    
-   `"options": [`
    
    -   `{}`
        
    
    `],`
    
-   `"vendor_id": "string"`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences/experience_id)Get experience

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences/experience_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/experiences/operation/get/catalog/experiences/experience_id!in=path&amp;path=experience_id&amp;t=request" id="tag/experiences/operation/get/catalog/experiences/experience_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences/experience_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/experiences/operation/get/catalog/experiences/experience_id!in=header&amp;path=accept&amp;t=request" id="tag/experiences/operation/get/catalog/experiences/experience_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/get/catalog/experiences/experience_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/experiences/operation/get/catalog/experiences/experience_id!in=header&amp;path=accept-version&amp;t=request" id="tag/experiences/operation/get/catalog/experiences/experience_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

get/supplier/catalog/experiences/{experience\_id}

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/catalog/experiences/{experience_id}'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`{`

-   `"archived": false,`
    
-   `"availability_slot_type": "DAILY",`
    
-   `"currency": "string",`
    
-   `"cutoff_time": "P0D",`
    
-   `"experience_id": "string",`
    
-   `"experience_name": "string",`
    
-   `"external_experience_id": "string",`
    
-   `"external_experience_name": "string",`
    
-   `"options": [`
    
    -   `{}`
        
    
    `],`
    
-   `"vendor_id": "string"`
    

`}`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id)Update experience

Updating an experience is limited to a small selection of properties.

Changes may take up to 24 hours to appear in the business platform and distribution sites.

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!in=path&amp;path=experience_id&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!in=header&amp;path=accept&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!in=header&amp;path=accept&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!in=header&amp;path=accept-version&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="archived"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!path=archived&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=archived&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=archived&amp;t=request"></a>archived</span></td><td><div><p><span></span><span>boolean</span></p><p><span>Default: </span><span>false</span></p><div><p>When an experience is archived, it is no longer for sale in Musement sites.</p><p>When an experience is un-archived, a member of the <em>Content Supplier Connectivity</em> team is required to un-archive the corresponding business platform activity.</p></div></div></td></tr><tr><td kind="field" title="cutoff_time"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!path=cutoff_time&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=cutoff_time&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=cutoff_time&amp;t=request"></a>cutoff_time</span></td><td><div><p><span></span><span>string</span><span> &lt;duration&gt;</span></p><p><span>Default: </span><span>"P0D"</span></p><div><p>The minimum amount of time required to book a travel date in advance.</p><p>This property must follow the <a href="https://www.iso.org/iso-8601-date-and-time-format.html">ISO 8601 standard</a>.</p></div></div></td></tr><tr><td kind="field" title="experience_name"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!path=experience_name&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=experience_name&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=experience_name&amp;t=request"></a>experience_name</span></td><td><div><p><span></span><span>string</span></p><div><p>The name of the experience as it will appear in PORTA.</p></div></div></td></tr><tr><td kind="field" title="external_experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!path=external_experience_id&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=external_experience_id&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=external_experience_id&amp;t=request"></a>external_experience_id</span></td><td><div><p><span></span><span>string</span></p><div><p>An additional ID for the experience which suppliers can use for their own records.</p></div></div></td></tr><tr><td kind="field" title="external_experience_name"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!path=external_experience_name&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=external_experience_name&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=external_experience_name&amp;t=request"></a>external_experience_name</span></td><td><div><p><span></span><span>string</span></p><div><p>An additional name for the experience which suppliers can use for their own records.</p></div></div></td></tr><tr><td kind="field" title="vendor_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/experiences/operation/patch/catalog/experiences/experience_id!path=vendor_id&amp;t=request" data-section-id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=vendor_id&amp;t=request" id="tag/experiences/operation/patch/catalog/experiences/experience_id!path=vendor_id&amp;t=request"></a>vendor_id</span></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The ID of the vendor that the experience belongs to.</p></div></div></td></tr></tbody></table>

patch/supplier/catalog/experiences/{experience\_id}

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"archived": false,`
    
-   `"cutoff_time": "P0D",`
    
-   `"experience_name": "string",`
    
-   `"external_experience_id": "string",`
    
-   `"external_experience_name": "string",`
    
-   `"vendor_id": "string"`
    

`}`

-   200
-   default

`{`

-   `"archived": false,`
    
-   `"availability_slot_type": "DAILY",`
    
-   `"currency": "string",`
    
-   `"cutoff_time": "P0D",`
    
-   `"experience_id": "string",`
    
-   `"experience_name": "string",`
    
-   `"external_experience_id": "string",`
    
-   `"external_experience_name": "string",`
    
-   `"options": [`
    
    -   `{}`
        
    
    `],`
    
-   `"vendor_id": "string"`
    

`}`
