---
# markdownlint-disable
# vale  off
layout: default
parent: sets resource
nav_order: 1
# tags used by AI files
description: PATCH existing `set` to the sets resource
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
    - PATCH /sets
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Patch existing set

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Partially updates an existing set in the [`sets`](./sets.md) resource.

As opposed to the `PUT` request or `POST` request,
a `PATCH` request only updates the entered attributes.
You do not need to enter all attributes to send a `PATCH` request.

## URL

```shell
{server_url}/sets
```

## cURL example

Patch an existing set. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PATCH http://localhost:3000/sets/27 \
  -H "Content-Type: application/json" \
  -d '{
    "pieces": 1850,
    "releaseYear": 2022
  }'
```

### cURL response

The response displays the following. Although you updated
only partial attributes of the resource, the response
contains all the attributes of the resource.

```json
{
  "id": 27,
  "setNumber": "10236",
  "name": "Shell Gas Station",
  "theme": "City",
  "pieces": 1850,
  "minifigures": 5,
  "releaseYear": 2022,
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

Patch an existing set. The changed values overwrite the existing values.

### Request

**Method**:

```shell
PATCH http://localhost:3000/sets/27
```

### Postman response

The response will display the set that you just patched.

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
