---
# markdownlint-disable
# vale  off
layout: default
parent: reference
# tags used by AI files
description: POST new `user` to the users resource
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
    - POST /users
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Post new user

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Posts a new user to the [`users`](users.md) resource.

## URL

```shell
{server_url}/users
```

## cURL example

Post a new user

### cURL command

```shell
curl -X POST http://localhost:3000/users/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 2,
    "name": "Scott Miller",
    "email": "scott@example.com",
    "joinDate": "2020-01-15",
    "collectionSize": 10,
    "favoriteTheme": "Icons"
  }'
```

### cURL response

The response displays:

```json
{
    "id": 2,
    "name": "Scott Miller",
    "email": "scott@example.com",
    "joinDate": "2020-01-15",
    "collectionSize": 10,
    "favoriteTheme": "Icons"
}
```

## Postman example

Post a new user.

### Request

**Method**:

```shell
POST http://localhost:3000/users/
```

### Postman response

The response will display the user that you just posted.

```json
{
    "id": 2,
    "name": "Scott Miller",
    "email": "scott@example.com",
    "joinDate": "2020-01-15",
    "collectionSize": 10,
    "favoriteTheme": "Icons"
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
