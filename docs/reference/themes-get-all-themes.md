---
# markdownlint-disable
# vale  off
layout: default
parent: Reference docs
# tags used by AI files
description: GET all `themes` from the themes resource
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /resource/themes
related_pages: []
examples: []
api_endpoints: 
    - GET /themes
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Get all themes

![BrickStack Reference](../../images/reference.png "BrickStack Reference")

Returns results for the [`themes`](../resource/themes.md) resource.
The results will contain all themes that are stored in the API.

## URL

```shell
{server_url}/themes
```

## cURL example

Get all themes.

### cURL command

```shell
curl http://localhost:3000/themes/
```

### cURL response

The response can contain multiple themes. For this document, only 1 theme is listed below:

```json
[
  {
    "id": 1,
    "name": "Creator Expert",
    "description": "Modular buildings and expert-level builds"
  }
]
```

## Postman example

Get all themes.

### Request

**Method**:

```shell
GET http://localhost:3000/themes/
```

### Postman response

The response can contain multiple themes. For this document, only 1 theme is listed below:

```json
[
    {
        "id": 1,
        "name": "Creator Expert",
        "description": "Modular buildings and expert-level builds"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 400 | Bad Request | There is an error with the format of the request |
| ERROR | ECONNREFUSED | The local server is not running (Postman) |
| Failed to connect | Failed to connect | The local server is not running (terminal / similar app)|
