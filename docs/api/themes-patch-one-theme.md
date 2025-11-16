---
# markdownlint-disable
# vale  off
layout: default
parent: themes resource
nav_order: 1
# tags used by AI files
description: PATCH existing `theme` to the themes resource
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
    - PATCH /themes
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Patch existing theme

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Partially updates an existing theme in the [`themes`](themes.md) resource.

As opposed to the `PUT` request or `POST` request,
a `PATCH` request only updates the entered attributes.
You do not need to enter all attributes to send a `PATCH` request.

## URL

```shell
{server_url}/themes/
```

## cURL example

Patch an existing theme. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PATCH http://localhost:3000/themes/7 \
  -H "Content-Type: application/json" \
  -d '{
    "description": "multiple build possibilities from 1 set"    
  }'
```

### cURL response

The response displays the following. Although you updated
only partial attributes of the resource, the response
contains all the attributes of the resource.

```json
{
  "id": 7,
  "name": "Creator 3in1",
  "description": "multiple build possibilities from 1 set"
}
```

## Postman example

Patch an existing theme. The changed values overwrite the existing values.

### Request

**Method**:

```shell
PATCH http://localhost:3000/themes/7/
```

### Postman response

The response will display the theme that you just patched.

```json
{
    "id": 7,
    "name": "Creator 3in1",
    "description": "multiple builds possible with just 1 set"
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
