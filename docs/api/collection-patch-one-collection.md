---
# markdownlint-disable
# vale  off
layout: default
parent: collection resource
nav_order: 1
# tags used by AI files
description: PATCH existing `collection` to the collection resource
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
    - PATCH /collection
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Patch existing collection

Partially updates an existing collection in the [`collection`](./collection.md) resource.

As opposed to the `PUT` request or `POST` request,
a `PATCH` request only updates the entered attributes.
You do not need to enter all attributes to send a `PATCH` request.

## URL

```shell
{server_url}/collection/
```

## cURL example

Patch an existing collection. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PATCH http://localhost:3000/collection/7 \
  -H "Content-Type: application/json" \
  -d '{
    "location": "basement",
    "notes": "Moved because it was taking up too much space"
  }'
```

### cURL response

The response displays the following. Although you updated
only partial attributes of the resource, the response
contains all the attributes of the resource.

```json
{
  "id": 7,
  "userId": 2,
  "setId": 6,
  "purchaseDate": "2025-01-01",
  "condition": "Built",
  "location": "basement",
  "notes": "Moved because it was taking up too much space"
}
```

## Postman example

Patch an existing collection. The changed values overwrite the existing values.

### Request

**Method**:

```shell
PATCH http://localhost:3000/collection/7/
```

### Postman response

The response will display the collection that you just patched.

```json
{
    "id": 7,
    "userId": 2,
    "setId": 6,
    "purchaseDate": "2025-01-01",
    "condition": "Built",
    "location": "basement",
    "notes": "Moved because it was taking up too much space"
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
