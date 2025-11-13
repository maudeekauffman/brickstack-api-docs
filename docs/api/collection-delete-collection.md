---
# markdownlint-disable
# vale  off
layout: default
parent: collection resource
nav_order: 1
# tags used by AI files
description: DELETE one `collection` from the collection resource
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
    - DELETE /collection
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Delete one collection

Deletes one collection from the [`collection`](./collection.md) resource.

## URL

```shell
{server_url}/collection/
```

## cURL example

Delete one specific collection.

### cURL command

```shell
curl -X DELETE http://localhost:3000/collection/7/
```

### cURL response

The response displays on the instance of the terminal that is running the server:

```shell
DELETE /collection/7/ 200 18.370 ms - 2
```

## Postman example

Delete one specific collection.

### Request

**Method**:

```shell
DELETE http://localhost:3000/collection/7/
```

### Postman response

The `body` area will display the symbols below and the `200 OK` indicator.

```json
{}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request to delete ID was successful |
| 400 | Bad Request | There is an error with the format of the request |
| 404 | Not found | The ID does not exist |
| ERROR | ECONNREFUSED | The local server is not running (Postman) |
| Failed to connect | Failed to connect | The local server is not running (terminal / similar app)|
