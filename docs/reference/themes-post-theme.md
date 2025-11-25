---
# markdownlint-disable
# vale  off
layout: default
parent: Reference docs
# tags used by AI files
description: POST new `theme` to the themes resource
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
    - POST /themes
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Post new theme

![BrickStack Reference](../../images/reference.png "BrickStack Reference")

Posts a new theme to the [`themes`](../resource/themes.md) resource.

## URL

```shell
{server_url}/themes/
```

## cURL example

Post a new theme.

### cURL command

```shell
curl -X POST http://localhost:3000/themes/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 7,
    "name": "Creator 3in1",
    "description": "multiple builds in one set"   
  }'
```

### cURL response

The response displays:

```json
{
  "id": 7,
  "name": "Creator 3in1",
  "description": "multiple builds in one set"
}
```

## Postman example

Post a new theme.

### Request

**Method**:

```shell
POST http://localhost:3000/themes/
```

### Postman response

The response will display the theme that you just posted.

```json
{
    "id": 7,
    "name": "Creator 3in1",
    "description": "multiple builds in one set"
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
