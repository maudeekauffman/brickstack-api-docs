---
# markdownlint-disable
# vale  off
layout: default
parent: reference
# tags used by AI files
description: PUT existing `user` to the users resource
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
    - PUT /users
version: "v1.0"
last_updated: "2025-12-11"
# vale  on
# markdownlint-enable
---

# Put existing user

![BrickStack Reference](../images/reference.png "BrickStack Reference")

Updates an existing user in the [`users`](users.md) resource.

## URL

```shell
{server_url}/users
```

## cURL example

Put an existing user. The changed values overwrite the existing values.

### cURL command

```shell
curl -X PUT http://localhost:3000/users/2 \
  -H "Content-Type: application/json" \
  -d '{
    "id": 2,
    "name": "Scott Miller",
    "email": "scott@example.com",
    "joinDate": "2021-01-01",
    "collectionSize": 20,
    "favoriteTheme": "Icons"
  }'
```

### cURL response

The response displays the following:

```json
{
  "id": 2,
  "name": "Scott Miller",
  "email": "scott@example.com",
  "joinDate": "2021-01-01",
  "collectionSize": 20,
  "favoriteTheme": "Icons"
}
```

## Postman example

Put an an existing user.

### Request

**Method**:

```shell
PUT http://localhost:3000/users/2
```

### Postman response

The response will display the user that you just put.

```json
{
  "id": 2,
  "name": "Scott Miller",
  "email": "scott@example.com",
  "joinDate": "2021-01-01",
  "collectionSize": 20,
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
