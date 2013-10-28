# Profile Resource

```json
{
    "id": {
        "summary": "The profile ID",
        "type": "String"
    },
    "display_name": {
        "summary": "The profile display name",
        "type": "String"
    },
    "name": {
        "summary": "The parts that make up the profile name",
        "type": "Object",
        "properties": {
            "family_name": {
                "summary": "Family name (last name in Western societies)",
                "type": "String"
            },
            "given_name": {
                "summary": "Given name (first name in Western societies)",
                "type": "String"
            },
            "middle_name": {
                "summary": "Middle name or names",
                "type": "String"
            }
        }
    },
    "email_addresses": {
        "summary": "The email addresses",
        "type": "Array",
        "item": {
            "value": {
                "summary": "The email address",
                "type": "Email"
            },
            "type": {
                "summary": "The type of address (eg. \"default\")",
                "type": "String"
            }
        }
    }
}
```

### Example
```json
{
    "id": "123abc",
    "display_name": "Joe Bloggs",
    "name": {
        "family_name": "Bloggs",
        "given_name": "Joe",
        "middle_name": null
    },
    "email_addresses": [
        {
            "value": "joe@example.com",
            "type": "default"
        }
    ]
}
```

### Endpoints used
 - **[`/profiles/{id}`](/endpoints/profiles/single.md)**
