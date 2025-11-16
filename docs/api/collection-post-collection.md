---
# markdownlint-disable
# vale  off
layout: default
parent: collection resource
nav_order: 1
# tags used by AI files
description: POST new `collection` to the collection resource
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
    - POST /collection
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Post new collection

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Posts a new collection to the [`collection`](./collection.md) resource.

## URL

```shell
{server_url}/collection/
```

## cURL example

Post a new collection.

### cURL command

```shell
curl -X POST http://localhost:3000/collection/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 6,
    "userId": 2,
    "setId": 4,
    "purchaseDate": "2025-01-01",
    "condition": "Not built",
    "location": "Basement",
    "notes": "Really excited to build this one"
}'
```

### cURL response

The response displays:

```json
{
  "id": 6,
  "userId": 2,
  "setId": 4,
  "purchaseDate": "2025-01-01",
  "condition": "Not built",
  "location": "Basement",
  "notes": "Really excited to build this one"
}
```

## Postman example

Post a new collection.

### Request

**Method**:

```shell
POST http://localhost:3000/collection/
```

### Postman response

The response will display the collection that you just posted.

```json
{
    "id": 7,
    "userId": 2,
    "setId": 6,
    "purchaseDate": "2025-01-01",
    "condition": "In progress",
    "location": "Basement",
    "notes": "I hope to finish it this weekend"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request to POST processed successfully |
| 400 | Bad Request | There is an error with the format of the request |
| ERROR | Insert failed, duplicate ID | The ID already exists |
| ERROR | ECONNREFUSED | The local server is not running (Postman) |
| Failed to connect | Failed to connect | The local server is not running (terminal / similar app) |
