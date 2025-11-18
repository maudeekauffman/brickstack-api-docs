---
# markdownlint-disable
# vale  off
layout: default
parent: collection resource
# tags used by AI files
description: PUT existing `collection` to the collection resource
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /api/collection
related_pages: []
examples: []
api_endpoints: 
    - PUT /collection
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Put existing collection

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Updates an existing collection in the [`collection`](./collection.md) resource.

## URL

```shell
{server_url}/collection/
```

## cURL example

Put an existing collection. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PUT http://localhost:3000/collection/7 \
  -H "Content-Type: application/json" \
  -d '{
    "id": 7,
    "userId": 2,
    "setId": 6,
    "purchaseDate": "2025-01-01",
    "condition": "Built",
    "location": "Living room",
    "notes": "Very exciting to build this"
}'
```

### cURL response

The response displays the following:

```json
{
  "id": 7,
  "userId": 2,
  "setId": 6,
  "purchaseDate": "2025-01-01",
  "condition": "Built",
  "location": "Living room",
  "notes": "Very exciting to build this"
}
```

## Postman example

Put an existing collection.

### Request

**Method**:

```shell
PUT http://localhost:3000/sets/7/
```

### Postman response

The response will display the collection that you just put.

```json
{
    "id": 7,
    "userId": 2,
    "setId": 6,
    "purchaseDate": "2025-01-01",
    "condition": "Built",
    "location": "Living room",
    "notes": "Very exciting to build this"
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
