# ajv errors

```json
[
  {
    "instancePath": "/0/local_action",
    "keyword": "type",
    "message": "must be string,object",
    "params": {
      "type": [
        "string",
        "object"
      ]
    },
    "schemaPath": "#/properties/local_action/type"
  },
  {
    "instancePath": "/0",
    "keyword": "required",
    "message": "must have required property 'block'",
    "params": {
      "missingProperty": "block"
    },
    "schemaPath": "#/required"
  },
  {
    "instancePath": "/0",
    "keyword": "anyOf",
    "message": "must match a schema in anyOf",
    "params": {},
    "schemaPath": "#/items/anyOf"
  }
]
```

# check-jsonschema

stdout:

```json
{
  "status": "fail",
  "errors": [
    {
      "filename": "negative_test/playbooks/tasks/local_action.yml",
      "path": "$[0]",
      "message": "{'local_action': []} is not valid under any of the given schemas",
      "has_sub_errors": true,
      "best_match": {
        "path": "$[0]",
        "message": "'block' is a required property"
      }
    }
  ]
}
```
