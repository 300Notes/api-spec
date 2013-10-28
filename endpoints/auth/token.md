# /auth/token
This endpoint provides an access token for a profile.
While native OAuth2 isn't implemented just yet, the specifics of this endpoint follow a similar pattern to allow for
future OAuth2 integration.

## POST://auth/token
This request is used to deliver access credentials for a specific profile.
### Request
#### Headers
```json
```
#### Body (Generic)
```json
{
    "client_id": {
        "summary": "The TrueLocal client ID",
        "type": "String"
    },
    "grant_type": {
        "summary": "The type of token grant requested",
        "type": "String",
        "enum": ["provider"]
    },
    ...
}
```
#### Body (Provider:Generic)
```json
{
    "client_id": {
        "summary": "The TrueLocal client ID",
        "type": "String"
    },
    "grant_type": {
        "summary": "The type of token grant requested",
        "type": "String",
        "value": "provider"
    },
    "provider": {
        "summary": "The name of the authentication provider",
        "type": "String",
        "enum": ["facebook"]
    },
    "details": {
        "summary": "The provider specific authentication details",
        "type": "Object"
    }
}
```
#### Body (Provider:Facebook)
```json
{
    "client_id": {
        "summary": "The TrueLocal client ID",
        "type": "String"
    },
    "grant_type": {
        "summary": "The type of token grant requested",
        "type": "String",
        "value": "provider"
    },
    "provider": {
        "summary": "The name of the authentication provider",
        "type": "String",
        "value": "facebook"
    },
    "details": {
        "summary": "The provider specific authentication details",
        "type": "Object",
        "properties": {
            "account_id": {
                "summary": "The Facebook account ID",
                "type": "String"
            },
            "access_token": {
                "summary": "The OAuth access token",
                "type": "String"
            },
            "refresh_token": {
                "summary": "The OAuth refresh token",
                "type": "String",
                "optional": "true"
            },
            "expires_in": {
                "summary": "The number of seconds until the access token expires",
                "type": "Number"
            }
        }
    }
}
```

### Response
#### Headers
```json
{
    "Status Code": {
        "summary": "One of \"200 OK\" or \"201 Created\"",
        "type": "Number",
        "enum": [200, 201]
    },
    "Location": {
        "summary": "The location of the profile resource",
        "type": "URI"
    }
}
```
#### Body
**[`Token`](/resources/token.md)**
