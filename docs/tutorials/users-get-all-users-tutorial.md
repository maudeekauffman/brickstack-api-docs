---
# markdownlint-disable
# vale  off
layout: default
parent: tutorials
nav_order: 3
# tags used by AI files
description: Get all `users` from the users resource
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites: 
    - /setup
    - /api/users
related_pages: []
examples: []
api_endpoints: 
    - GET /users
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: Get all users

![BrickStack Tutorial](../images/tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `GET /users` endpoint to get all
existing users from the BrickStack API.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/users` resource
- Use GitBash to interact with the `/users` resource
- GET all existing users

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to `GET` all existing users from the service.

### 1. Understand the URL to the users resource

Before you GET all users from the BrickStack API, you must understand how
to call the users resource. The link to the users resource is:
`http://localhost:3000/users/`.

### 2. Create the GET request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `GET`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/users/`
4. In the top right-hand corner, click `Send`
5. Check the bottom part of the screen
6. If you have an error: correct the mistake based on the response text that you get
7. If you do not have an error: you receive a response
with with details about all users.
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the GET request in GitBash

1. Open GitBash
2. Enter the command `curl http://localhost:3000/users/`
3. Press the `enter` key
4. View the response from GitBash
5. If you have an error: correct the mistake based on the response text that you get
6. If you do not have an error: you receive a response with details about all users.

### 4. View the response - Postman

You receive a response.

If you receive a response without an error, the users
appear at the bottom part of the screen.
A green rectangle
with the text `200 OK` also appears.

Here is an example response when only 1 user is in the API:

```json
[
    {
        "id": 1,
        "name": "Maudie Kauffman",
        "email": "maudie@example.com",
        "joinDate": "2020-01-15",
        "collectionSize": 24,
        "favoriteTheme": "Icons"
    }
]
```

Here is an example response with 3 users from the API:

```json
[
    {
        "id": 1,
        "name": "Maudie Kauffman",
        "email": "maudie@example.com",
        "joinDate": "2025-01-15",
        "collectionSize": 25,
        "favoriteTheme": "Icons"
    },
    [
        {
            "id": 2,
            "name": "Scott Miller",
            "email": "scott@example.com",
            "joinDate": "2020-01-15",
            "collectionSize": 24,
            "favoriteTheme": "Icons"
        }
    ],
    {
        "id": 3,
        "name": "John Doe",
        "email": "john@example.com",
        "joinDate": "2025-01-15",
        "collectionSize": 25,
        "favoriteTheme": "Icons"
    }
]
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

If you receive a response without an error, details about all users
appear.

Here is an example response when only 1 user is in the API:

```json
{
  "id": 1,
  "name": "Maudie Kauffman",
  "email": "maudie@example.com",
  "joinDate": "2025-01-15",
  "collectionSize": 25,
  "favoriteTheme": "Icons"
}
```

Here is an example response with 3 users from the API:

```json
[
  {
    "id": 1,
    "name": "Maudie Kauffman",
    "email": "maudie@example.com",
    "joinDate": "2025-01-15",
    "collectionSize": 25,
    "favoriteTheme": "Icons"
  },
  [
    {
      "id": 2,
      "name": "Scott Miller",
      "email": "scott@example.com",
      "joinDate": "2020-01-15",
      "collectionSize": 24,
      "favoriteTheme": "Icons"
    }
  ],
  {
    "id": 3,
    "name": "John Doe",
    "email": "john@example.com",
    "joinDate": "2025-01-15",
    "collectionSize": 25,
    "favoriteTheme": "Icons"
  }
]
```

If there was an error, the error text appears.

## Completion and validation

If you received a response with no errors, you have successfully used the `GET` command.

If you received an error, read the text of the error. Errors might be due to:

- You entered the incorrect server URL
- Invalid syntax of the GitBash command

## Next steps

Now that you have used `GET` to get all existing users,
you can explore more of the API:

- Try getting one user
- View other tutorials
- View the [users API reference document](../api/users.md)
  