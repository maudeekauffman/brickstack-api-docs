---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
# tags used by AI files
description: Patch an existing `users` resource
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
    -  PATCH /users
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: PATCH an existing user

![BrickStack Tutorial](../../images/tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `PATCH /users` endpoint to update an existing
user on the BrickStack API.

The `PATCH` command will update a user with the entered user ID.

As opposed to the `PUT` request or `POST` request,
a `PATCH` request only updates the entered attributes.
You do not need to enter all attributes to send a `PATCH` request.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/users` resource
- Use GitBash to interact with the `/users` resource
- PATCH an existing user

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to PATCH an existing user on the service.

### 1. Understand user format

Before you PATCH a user on the BrickStack API, you must understand the
format of an existing user. Refer to the examples below.

#### For Postman

```json
  {
        "id": 4,
        "name": "Bob Loblaw",
        "email": "bob@example.com",
        "joinDate": "2025-01-01",
        "collectionSize": 10,
        "favoriteTheme": "Icons"
   }
```

#### For GitBash

```shell
curl -X PATCH http://localhost:3000/users/4/ \
  -H "Content-Type: application/json" \
  -d '{
   "id": 4,
    "name": "Bob Loblaw",
    "email": "bob@example.com",
    "joinDate": "2025-01-01",
    "collectionSize": 10,
    "favoriteTheme": "Icons"    
}'
  ```

Because you are only updating partial attributes,
you do not have to enter every attribute as listed above.

### 2. Create the PATCH request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `PATCH`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/users/4/`
4. Below the URL that you entered, click on the `Body` tab
5. Change the format to `raw`
6. Copy the user from section 1 of this document
7. Change the attributes that you want to, delete any lines that you do not want to update
8. Paste the user
9. In the top right-hand corner, click `Send`
10. Check the bottom part of the screen
11. If you have an error: correct the mistake based on the response text that you get
12. If you do not have an error: you receive a response
with the data that you just sent.
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the PATCH request in GitBash

1. Open GitBash
2. Copy the GitBash command from section 1 of this document
3. Paste the command in Notepad or a similar program
4. Change / delete the attributes that you want to and copy the newly-changed user
5. Paste the GitBash command
6. Press the `enter` key
7. View the response from GitBash
8. If you have an error: correct the mistake based on the response text that you receive
9. If you do not have an error: you receive a response

### 4. View the response - Postman

You receive a response.

If you successfully patched the user, the user
appears at the bottom of the screen.
A green rectangle
with the text `200 OK` also appears.

Here is an example response:

```json
{
    "id": 4,
    "name": "Bob Loblaw",
    "email": "bob@example.com",
    "joinDate": "2025-01-01",
    "collectionSize": 10,
    "favoriteTheme": "Icons"
}
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

Here is an example response:

```json
{
  "id": 4,
  "name": "Bob Loblaw",
  "email": "bob@example.com",
  "joinDate": "2025-01-01",
  "collectionSize": 10,
  "favoriteTheme": "Icons"
}
```

If there was an error, the error text appears.

## Completion and validation

If you received a response with no errors, you have used the `PATCH` command
to partially update an existing user.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- Invalid syntax of the GitBash command
- The local server is not running

## Next steps

Now that you have used the `PATCH` command to update a user,
you can explore more of the API:

- Try posting a new user
- View other tutorials
- View the [users API resource document](../resource/users.md)
  