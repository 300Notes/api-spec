# /profiles/{id}
This endpoint provides access to the details of a specific profile.

## GET://profiles/{id}
This request is used to retrieve a specific profile. The authenticated user must be authorized to view the specific
profile for a successful response.
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
        "summary": "200 OK",
        "type": "Number",
        "value": 200
    }
}
```
#### Body
**[`Profile`](/resources/profile.md)**
