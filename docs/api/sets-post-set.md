---
# markdownlint-disable
# vale  off
layout: default
parent: sets resource
nav_order: 1
# tags used by AI files
description: POST new `set` to the sets resource
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
    - POST /sets
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Post new set

Returns results for the [`sets`](./sets.md) resource.
The results will contain all LEGO sets that are stored in the API.

## URL

```shell
{server_url}/sets
```

## cURL example

Post a new set.

### cURL command

```shell
curl -X POST http://localhost:3000/sets/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 30,
    "setNumber": "10236",
    "name": "Texaco Gas Station",
    "theme": "City",
    "pieces": 1700,
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
  }'
```

### cURL response

The response will be shown on your instance of the terminal that is running the server:

```shell
POST /sets/ 201 34.494 ms - 264
```

## Postman example

Post a new set.

### Request

**Method**:

```shell
POST http://localhost:3000/sets/
```

### Postman response

The response will display the set that you just posted.

```json
{
    "id": 30,
    "setNumber": "10236",
    "name": "Texaco Gas Station",
    "theme": "City",
    "pieces": 1700,
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
| 200 | Success | Requested data returned successfully |
| 400 | Bad Request | There is an error with the format of the request |
| ERROR | ECONNREFUSED | The local server is not running (Postman) |
| Failed to connect | Failed to connect | The local server is not running (terminal / similar app)|
