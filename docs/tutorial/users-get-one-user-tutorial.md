---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 20
# tags used by AI files
description: Get one `user` from the users resource
tags:
    - api
categories: 
    - tutorials
ai_relevance: high
importance: 6
prerequisites: 
    - /setup
    - /resource/users
related_pages: []
examples: []
api_endpoints: 
    - GET /users
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: Get one user

![BrickStack Tutorial](../../images/tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `GET /users` endpoint to get an
existing user from the BrickStack API.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/users` resource
- Use GitBash to interact with the `/users` resource
- GET an existing user

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to `GET` an existing user from the service.

### 1. Understand the URL to the users resource

Before you GET a user from the BrickStack API, you must understand how
to call the user resource. The link to a specific user is:
`http://localhost:3000/users/1/` This link makes a request
for the user with the ID `1`.

### 2. Create the GET request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `GET`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/users/1/`
4. In the top right-hand corner, click `Send`
5. Check the bottom part of the screen
6. If you have an error: correct the mistake based on the response text that you get
7. If you do not have an error: you receive a response
with with details about a user.
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the GET request in GitBash

1. Open GitBash
2. Enter the command `curl http://localhost:3000/users/1/`
3. Press the `enter` key
4. View the response from GitBash
5. If you have an error: correct the mistake based on the response text that you get
6. If you do not have an error: you receive a response with details about the user.

### 4. View the response - Postman

You receive a response.

If you receive a response without an error, the user
appears at the bottom part of the screen.
A green rectangle
with the text `200 OK` also appears.

Here is an example response:

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

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

If you receive a response without an error, details about the user
appear.

Here is an example response:

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

If there was an error, the error text will appear.

## Completion and validation

If you received a response with no errors, you have successfully used the `GET` command.

If you received an error, read the text of the error. Errors might be due to:

- The entered user ID does not exist
- Invalid syntax of the GitBash command

## Next steps

Now that you have used the `GET` command to get an existing user,
you can explore more of the API:

- Try getting all users
- View other tutorials
- View the [users API resource document](../resource/users.md)
  