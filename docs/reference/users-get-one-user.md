---
# markdownlint-disable
# vale  off
layout: default
parent: Reference docs
nav_order: 20
# tags used by AI files
description: GET one `user` from the users resource
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites:
    - /resource/users
related_pages: []
examples: []
api_endpoints: 
    - GET /users
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Get one user

![BrickStack Reference](../../images/reference.png "BrickStack Reference")

Returns one result for the [`users`](../resource/users.md) resource.
The results will contain one user that is stored in the API.

## URL

```shell
{server_url}/users
```

## cURL example

Get a specific user.

### cURL command

```shell
curl http://localhost:3000/users/1
```

### cURL response

```json
{
  "id": 1,
  "name": "Maudie Kauffman",
  "email": "maudie@example.com",
  "joinDate": "2020-01-15",
  "collectionSize": 24,
  "favoriteTheme": "Icons"
}
```

## Postman example

Get a specific user.

### Request

**Method**:

```shell
GET http://localhost:3000/users/1
```

### Postman response

```json
{
    "id": 1,
    "name": "Maudie Kauffman",
    "email": "maudie@example.com",
    "joinDate": "2020-01-15",
    "collectionSize": 24,
    "favoriteTheme": "Icons"
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
