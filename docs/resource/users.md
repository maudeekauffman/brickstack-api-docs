---
# markdownlint-disable
# vale  off
layout: default
nav_order: 4
parent: Resource docs
# tags used by AI files
description: "Information about the `users` resource"
tags: 
    - api
categories: 
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/users
examples: []
api_endpoints:
    - /users
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# `users` resource

![BrickStack Resource](./resource.png "BrickStack Resource")

Base endpoint:

```shell
{server_url}/users
```

Contains information about available users in the BrickStack API.

Users are needed for the API to be able to track collections per user.

## Resource properties

Sample `users` resource

```js
{
      "id": 1,
      "name": "Maudie Kauffman",
      "email": "maudie@example.com",
      "joinDate": "2020-01-15",
      "collectionSize": 24,
      "favoriteTheme": "Icons"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The ID of the user |
| `name` | string | The name of the user |
| `email` | string | The email address of the user |
| `joinDate` | string | The date when the user was added to the BrickStack API |
| `collectionSize` | string | The number of LEGO sets for the collection of this user |
| `favoriteTheme` | string | The favorite LEGO set theme for this user |

## READ

* [Get all users](../tutorial/users-get-all-users-tutorial.md)
* [Get a specific user](../tutorial/users-get-one-user-tutorial.md)
