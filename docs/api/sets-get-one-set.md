---
# markdownlint-disable
# vale  off
layout: default
parent: sets resource
nav_order: 1
# tags used by AI files
description: GET one `sets` from the sets resource
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
    - GET /sets
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Get one set

Returns one result for the [`sets`](./sets.md) resource.
The results will contain one LEGO set that is stored in the API.

## URL

```shell
{server_url}/sets
```

## cURL example

Get a specific set.

### cURL command

```shell
curl http://localhost:3000/sets/1
```

### cURL response

```json
{
  "id": 1,
  "setNumber": "10234",
  "name": "Sydney Opera House",
  "theme": "Creator Expert",
  "pieces": 1929,
  "minifigures": 0,
  "releaseYear": 2013,
  "ageRange": "16+",
  "price": 324.99,
  "retired": true,
  "tags": [
    "architecture",
    "landmark",
    "australia"
  ]
}
```

## Postman example

Get a specific set.

### Request

**Method**:

```shell
GET http://localhost:3000/sets/1
```

### Postman response

```json
{
    "id": 1,
    "setNumber": "10234",
    "name": "Sydney Opera House",
    "theme": "Creator Expert",
    "pieces": 1929,
    "minifigures": 0,
    "releaseYear": 2013,
    "ageRange": "16+",
    "price": 324.99,
    "retired": true,
    "tags": [
        "architecture",
        "landmark",
        "australia"
    ]
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 400 | Bad Request | There is an error with the format of the request |
| ERROR | ECONNREFUSED | The local server is not running (Postman) |
| Failed to connect | Failed to connect | The local server is not running (terminal / similar app) |
