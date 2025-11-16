---
# markdownlint-disable
# vale  off
layout: default
parent: users resource
nav_order: 1
# tags used by AI files
description: DELETE one `user` from the users resource
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /api/users
related_pages: []
examples: []
api_endpoints: 
    - DELETE /users
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Delete one user

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Deletes one user from the [`users`](users.md) resource.

## URL

```shell
{server_url}/users
```

## cURL example

Delete one specific user.

### cURL command

```shell
curl -X DELETE http://localhost:3000/users/2
```

### cURL response

The response displays on the instance of the terminal that is running the server:

```shell
DELETE /users/2 200 11.104 ms - 2
```

## Postman example

Delete one specific user.

### Request

**Method**:

```shell
DELETE http://localhost:3000/users/3
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
