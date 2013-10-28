# Token Resource

```json
{
    "access_token": {
        "summary": "The access token to use throughout the session",
        "type": "String"
    },
    "refresh_token": {
        "summary": "The refresh token",
        "type": "String"
    },
    "expires_in": {
        "summary": "The number of seconds until the access token expires",
        "type": "Number"
    },
    "token_type": {
        "summary": "The type of access token",
        "type": "String",
        "enum": ["Bearer"]
    }
}
```

### Example
```json
{
    "access_token": "123abc",
    "refresh_token": "456def",
    "expires_in": 3600,
    "token_type": "Bearer"
}
```

### Endpoints used
 - [`/auth/token`](/spec/endpoints/auth/token.md)
