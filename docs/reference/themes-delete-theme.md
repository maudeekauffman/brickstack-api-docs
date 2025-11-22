---
# markdownlint-disable
# vale  off
layout: default
parent: reference
# tags used by AI files
description: DELETE one `theme` from the themes resource
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
    - DELETE /themes
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Delete one theme

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Deletes one theme from the [`themes`](themes.md) resource.

## URL

```shell
{server_url}/themes/
```

## cURL example

Delete one specific theme.

### cURL command

```shell
curl -X DELETE http://localhost:3000/themes/7/
```

### cURL response

The response displays on the instance of the terminal that is running the server:

```shell
DELETE /themes/7/ 200 26.691 ms - 2
```

## Postman example

Delete one specific theme.

### Request

**Method**:

```shell
DELETE http://localhost:3000/themes/7/
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
