---
created: 2024-08-06T01:12:42 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/openapi/tag/mandatory-questions/
author: 
---

# Daily slots

> ## Excerpt
> Customers must select a date for a booking.

---
Customers must select a date for a booking.

## [](https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots)Get daily slots for option

The `date_from` and `date_to` query parameters permit up to two years of dates.

Security**Supplier-production** or **Supplier-sandbox**

##### path Parameters

<table><tbody><tr><td kind="field" title="experience_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=path&amp;path=experience_id&amp;t=request" data-section-id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=path&amp;path=experience_id&amp;t=request" id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=path&amp;path=experience_id&amp;t=request"></a>experience_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr><tr><td kind="field" title="option_id"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=path&amp;path=option_id&amp;t=request" data-section-id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=path&amp;path=option_id&amp;t=request" id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=path&amp;path=option_id&amp;t=request"></a>option_id</span><p>required</p></td><td><div><p><span></span><span>string</span><span>^(?!\-|\.|\_)[0-9a-z\-\.\_]{1,50}$</span></p></div></td></tr></tbody></table>

##### query Parameters

<table><tbody><tr><td kind="field" title="date_from"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=query&amp;path=date_from&amp;t=request" data-section-id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=query&amp;path=date_from&amp;t=request" id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=query&amp;path=date_from&amp;t=request"></a>date_from</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;date&gt;</span></p><div><p>Filters results to those which take place on or after the specified date.</p></div></div></td></tr><tr><td kind="field" title="date_to"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=query&amp;path=date_to&amp;t=request" data-section-id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=query&amp;path=date_to&amp;t=request" id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=query&amp;path=date_to&amp;t=request"></a>date_to</span><p>required</p></td><td><div><p><span></span><span>string</span><span> &lt;date&gt;</span></p><div><p>Filters results to those which take place on or before the specified date.</p></div></div></td></tr></tbody></table>

##### header Parameters

<table><tbody><tr><td kind="field" title="accept"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=header&amp;path=accept&amp;t=request" data-section-id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=header&amp;path=accept&amp;t=request" id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=header&amp;path=accept&amp;t=request"></a>accept</span><p>required</p></td><td><div><p><span></span><span>string</span></p><div><p>Specify the format of the response.</p></div><p><span>Value:</span> <span>"application/json"</span></p></div></td></tr><tr><td kind="field" title="accept-version"><span><a href="https://porta.redoc.ly/openapi/tag/mandatory-questions/#tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=header&amp;path=accept-version&amp;t=request" data-section-id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=header&amp;path=accept-version&amp;t=request" id="tag/daily-slots/operation/get/availability/experiences/experience_id/options/option_id/slots/daily_slots!in=header&amp;path=accept-version&amp;t=request"></a>accept-version</span><p>required</p></td><td><div><p><span></span><span>string</span><span> (PORTA version)</span></p><div><p>The version of PORTA for the request.</p></div><div><table><thead><tr><th><span>Value:</span></th><th><strong>Description</strong></th></tr></thead><tbody><tr><td>vnd.porta-api.v1</td><td><span><p>Version 1.0.0</p></span></td></tr></tbody></table></div></div></td></tr></tbody></table>

200

Daily slots for option

get/supplier/availability/experiences/{experience\_id}/options/{option\_id}/slots/daily\_slots

-   curl
-   C#
-   Node.js

```
<span>curl</span> <span>-i</span> <span>-X</span> GET <span>\</span>
  <span>'https://prod.api.tui/tui-musement-porta/supplier/availability/experiences/{experience_id}/options/{option_id}/slots/daily_slots?date_from=2019-08-24&amp;date_to=2019-08-24'</span> <span>\</span>
  <span>-H</span> <span>'Authorization: Bearer &lt;YOUR_TOKEN_HERE&gt;'</span> <span>\</span>
  <span>-H</span> <span>'accept: application/json'</span> <span>\</span>
  <span>-H</span> <span>'accept-version: vnd.porta-api.v1'</span>
```

-   200
-   default

`[`

-   `{`
    
    -   `"available_holder_categories": [],`
        
    -   `"guide_languages": [],`
        
    -   `"option_id": "string",`
        
    -   `"slot_id": "string",`
        
    -   `"capacity": 0,`
        
    -   `"daily_slot": {}`
        
    
    `}`
    

`]`
