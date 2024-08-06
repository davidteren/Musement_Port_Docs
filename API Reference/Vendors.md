---
created: 2024-08-06T01:13:04 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# Vendors

> ## Excerpt
> Suppliers can use vendors to indicate when experiences are sourced differently.

---
## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/get/vendors)Get vendors

Security**Supplier-production** or **Supplier-sandbox**

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/get/vendors!in=header&amp;path=accept&amp;t=request" data-section-id="tag/vendors/operation/get/vendors!in=header&amp;path=accept&amp;t=request" id="tag/vendors/operation/get/vendors!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/get/vendors!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/vendors/operation/get/vendors!in=header&amp;path=accept-version&amp;t=request" id="tag/vendors/operation/get/vendors!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  https://prod.api.tui/tui-musement-porta/supplier/vendors <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`[`

-   `{`
    
    -   `"name": "string",`
        
    -   `"vendor_id": "string"`
        
    
    `}`
    

`]`

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/post/vendors)Create vendor

Security**Supplier-production** or **Supplier-sandbox**

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/post/vendors!in=header&amp;path=accept&amp;t=request" data-section-id="tag/vendors/operation/post/vendors!in=header&amp;path=accept&amp;t=request" id="tag/vendors/operation/post/vendors!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/post/vendors!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/vendors/operation/post/vendors!in=header&amp;path=accept-version&amp;t=request" id="tag/vendors/operation/post/vendors!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

##### Request Body schema: application/json

<table><tbody><tr><td kind="field" title="name"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/post/vendors!path=name&amp;t=request" data-section-id="tag/vendors/operation/post/vendors!path=name&amp;t=request" id="tag/vendors/operation/post/vendors!path=name&amp;t=request"></a>name</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>The name of the vendor as it will appear in PORTA.</p></div></div></td></tr><tr><td kind="field" title="vendor_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/vendors/operation/post/vendors!path=vendor_id&amp;t=request" data-section-id="tag/vendors/operation/post/vendors!path=vendor_id&amp;t=request" id="tag/vendors/operation/post/vendors!path=vendor_id&amp;t=request"></a>vendor_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p><div><p>The vendor ID, assigned by the supplier.</p></div></div></td></tr></tbody></table>

-   Payload
-   curl
-   C#
-   Node.js

`{`

-   `"name": "string",`
    
-   `"vendor_id": "string"`
    

`}`

-   200
-   default

`{`

-   `"name": "string",`
    
-   `"vendor_id": "string"`
    

`}`
