# /auth/profile
This endpoint provides details of the authenticated profile.

## GET://auth/profile
This request is used to deliver the location of the authenticated profile as a method of convenience only.
### Request
#### Headers
```json
{
    "Authentication": {
        "summary": "The client authentication",
        "type": "String",
        "pattern": "<token_type> <access_token>"
    }
}
```
#### Body
```json
```

### Response
#### Headers
```json
{
    "Status Code": {
        "summary": "303 See Other",
        "type": "Number",
        "value": 303
    },
    "Location": {
        "summary": "The location of the profile resource",
        "type": "URI"
    }
}
```
#### Body
```json
```
