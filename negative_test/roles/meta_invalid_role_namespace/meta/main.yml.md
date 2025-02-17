# ajv errors

```json
[
  {
    "instancePath": "",
    "keyword": "type",
    "message": "must be null",
    "params": {
      "type": "null"
    },
    "schemaPath": "#/anyOf/0/type"
  },
  {
    "instancePath": "/galaxy_info/namespace",
    "keyword": "pattern",
    "message": "must match pattern \"^[a-z][a-z0-9_]+$\"",
    "params": {
      "pattern": "^[a-z][a-z0-9_]+$"
    },
    "schemaPath": "#/properties/namespace/pattern"
  },
  {
    "instancePath": "",
    "keyword": "anyOf",
    "message": "must match a schema in anyOf",
    "params": {},
    "schemaPath": "#/anyOf"
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
      "filename": "negative_test/roles/meta_invalid_role_namespace/meta/main.yml",
      "path": "$",
      "message": "{'galaxy_info': {'description': 'foo', 'min_ansible_version': '2.9', 'namespace': 'foo-bar', 'company': 'foo', 'license': 'MIT', 'platforms': [{'name': 'Alpine', 'versions': ['all']}]}} is not valid under any of the given schemas",
      "has_sub_errors": true,
      "best_match": {
        "path": "$",
        "message": "{'galaxy_info': {'description': 'foo', 'min_ansible_version': '2.9', 'namespace': 'foo-bar', 'company': 'foo', 'license': 'MIT', 'platforms': [{'name': 'Alpine', 'versions': ['all']}]}} is not of type 'null'"
      }
    }
  ]
}
```
