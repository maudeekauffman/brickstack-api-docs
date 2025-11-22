---
# markdownlint-disable
# vale  off
layout: default
parent: reference
# tags used by AI files
description: PATCH existing `user` to the users resource
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
    - PATCH /users
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Patch existing user

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Partially updates an existing user in the [`users`](users.md) resource.

As opposed to the `PUT` request or `POST` request,
a `PATCH` request only updates the entered attributes.
You do not need to enter all attributes to send a `PATCH` request.

## URL

```shell
{server_url}/users
```

## cURL example

Patch an existing user. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PATCH http://localhost:3000/users/2 \
  -H "Content-Type: application/json" \
  -d '{
    "joinDate": "2025-12-12"    
  }'
```

### cURL response

The response displays the following. Although you updated
only partial attributes of the resource, the response
contains all the attributes of the resource.

```json
{
  "id": 2,
  "name": "Scott Miller",
  "email": "scott@example.com",
  "joinDate": "2025-12-12",
  "collectionSize": 100,
  "favoriteTheme": "Icons"
}
```

## Postman example

Patch an existing user. The changed values overwrite the existing values.

### Request

**Method**:

```shell
PATCH http://localhost:3000/users/2
```

### Postman response

The response will display the user that you just patched.

```json
{
    "id": 2,
    "name": "Scott Miller",
    "email": "scott@example.com",
    "joinDate": "2020-12-12",
    "collectionSize": 101,
    "favoriteTheme": "Icons"
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
