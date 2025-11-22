---
# markdownlint-disable
# vale  off
layout: default
parent: reference
# tags used by AI files
description: PUT existing `set` to the sets resource
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /api/sets
related_pages: []
examples: []
api_endpoints: 
    - PUT /sets
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Put existing set

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Updates an existing set in the [`sets`](./sets.md) resource.

## URL

```shell
{server_url}/sets
```

## cURL example

Put an existing set. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PUT http://localhost:3000/sets/27 \
  -H "Content-Type: application/json" \
  -d '{
    "id": 27,
    "setNumber": "10400",
    "name": "Shell Gas Station",
    "theme": "City",
    "pieces": 1700,
    "minifigures": 5,
    "releaseYear": 2025,
    "ageRange": "16+",
    "price": 250,
    "retired": false,
    "tags": [
      "city",
      "store",
      "vehicles"
    ]
  }'
```

### cURL response

The response displays the following:

```json
{
  "id": 27,
  "setNumber": "10236",
  "name": "Shell Gas Station",
  "theme": "City",
  "pieces": 1715,
  "minifigures": 5,
  "releaseYear": 2025,
  "ageRange": "16+",
  "price": 200,
  "retired": false,
  "tags": [
    "city",
    "store",
    "vehicles"
  ]
}
```

## Postman example

Put an existing set.

### Request

**Method**:

```shell
PUT http://localhost:3000/sets/27
```

### Postman response

The response will display the set that you just put.

```json
{
  "id": 27,
  "setNumber": "10236",
  "name": "Shell Gas Station",
  "theme": "City",
  "pieces": 1715,
  "minifigures": 5,
  "releaseYear": 2025,
  "ageRange": "16+",
  "price": 200,
  "retired": false,
  "tags": [
    "city",
    "store",
    "vehicles"
  ]
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request to POST processed successfully |
| 400 | Bad Request | There is an error with the format of the request |
| 404 | Not found | The ID does not exist |
| ERROR | ECONNREFUSED | The local server is not running (Postman) |
| Failed to connect | Failed to connect | The local server is not running (terminal / similar app) |
