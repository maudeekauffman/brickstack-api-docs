---
# markdownlint-disable
# vale  off
layout: default
parent: Reference docs
# tags used by AI files
description: PUT existing `theme` to the themes resource
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
    - PUT /themes
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Put existing theme

![BrickStack Reference](../../images/reference.png "BrickStack Reference")

Updates an existing theme in the [`themes`](../resource/themes.md) resource.

## URL

```shell
{server_url}/themes/
```

## cURL example

Put an existing theme. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PUT http://localhost:3000/themes/7 \
  -H "Content-Type: application/json" \
  -d '{
    "id": 7,
    "name": "Creator 3in1",
    "email": "scott@example.com",
    "description": "multiple builds in 1 set"
  }'
```

### cURL response

The response displays the following:

```json
{
  "id": 7,
  "name": "Creator 3in1",
  "email": "scott@example.com",
  "description": "multiple builds in 1 set"
}
```

## Postman example

Put an an existing theme.

### Request

**Method**:

```shell
PUT http://localhost:3000/themes/7
```

### Postman response

The response will display the theme that you just put.

```json
{
    "id": 7,
    "name": "Creator 3in1",
    "description": "multiple builds in 1 set"
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
