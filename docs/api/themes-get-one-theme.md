---
# markdownlint-disable
# vale  off
layout: default
parent: themes resource
nav_order: 1
# tags used by AI files
description: GET one `theme` from the themes resource
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /api/themes
related_pages: []
examples: []
api_endpoints: 
    - GET /themes
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Get one theme

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Returns one result for the [`theme`](themes.md) resource.
The results will contain one theme that is stored in the API.

## URL

```shell
{server_url}/themes
```

## cURL example

Get a specific theme

### cURL command

```shell
curl http://localhost:3000/themes/1/
```

### cURL response

```json
{
  "id": 1,
  "name": "Creator Expert",
  "description": "Modular buildings and expert-level builds"
}
```

## Postman example

Get a specific theme.

### Request

**Method**:

```shell
GET http://localhost:3000/themes/1/
```

### Postman response

```json
{
    "id": 1,
    "name": "Creator Expert",
    "description": "Modular buildings and expert-level builds"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 400 | Bad Request | There is an error with the format of the request |
| 404 | Not found | The ID does not exist |
| ERROR | ECONNREFUSED | The local server is not running (Postman) |
| Failed to connect | Failed to connect | The local server is not running (terminal / similar app) |
