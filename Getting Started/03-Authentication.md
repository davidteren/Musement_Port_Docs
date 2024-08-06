---
created: 2024-07-15T22:48:41 (UTC +02:00)
tags: []
source: https://porta.redoc.ly/getting-started/
author: 
---

# Authentication

> ## Excerpt
> Use OAuth 2.0 to receive an access token so that you can use PORTA.

---
Last updated 2 months ago

Authentication must be the first step before making any other API request.

PORTA uses the **OAuth 2.0** authorization framework to give applications access to the API. Check out [RFC-6749][1] and [DigitalOcean][2] for an in-depth overview of the framework.

Suppliers are assigned an access key and secret key to use for the initial authentication request:

```bash
curl 'https://prod.api.tui/oauth2/token' \ -H 'Content-Type: application/x-www-form-urlencoded' \ -d 'client_id={accessKey}' \ -d 'client_secret={secretKey}' \ -d 'grant_type=client_credentials'
```

##### Content-Type

Note the `Content-Type` header in the request above. This endpoint does not accept other header values, such as `application/json`.

A successful response returns an `access_token` property to use for all subsequent API requests. The `token_type` property in the response indicates how to use token and the `expires_in` property communicates how long the token will last.

In the example response below, we are given an access token that will last one hour:

```json
{ "token_type": "Bearer", "access_token": "FnxKF4w47kq2McBs4eP48kqB9KgX", "client_id": "KSc6yRCwWpTq4xdrQL5mxxGgve23WBJK", "scope": "musement-porta-product.write musement-porta-product.all musement-porta-product.read", "expires_in": 3599, "issued_at": 1678189085804 }
```

The `token_type` value of `bearer` in the above example means the token must be added to the `Authorization` HTTP header, preceded by the word `Bearer` and a space:

```bash
curl '{baseUrl}/supplier/catalog/experiences' \ -H 'accept: application/json' \ -H 'accept-version: vnd.porta-api.v1' \ -H 'Authorization: Bearer FnxKF4w47kq2McBs4eP48kqB9KgX'
```

When a token expires, repeat the authentication process to receive a new valid token.

[1]: https://datatracker.ietf.org/doc/html/rfc6749
[2]: https://www.digitalocean.com/community/tutorials/an-introduction-to-oauth-2
