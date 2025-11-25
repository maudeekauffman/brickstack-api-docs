---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 11
# tags used by AI files
description: Patch an existing `sets` resource
tags:
    - api
categories: 
    - tutorials
ai_relevance: high
importance: 6
prerequisites: 
    - /setup
    - /resource/sets
related_pages: []
examples: []
api_endpoints: 
    -  PATCH /sets
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: Patch an existing set

![BrickStack Tutorial](../../images/tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `PATCH /sets` endpoint to update an existing
LEGO set on the BrickStack API.

The `PATCH` command will update a set with the entered set ID.

As opposed to the `PUT` request or `POST` request,
a `PATCH` request only updates the entered attributes.
You do not need to enter all attributes to send a `PATCH` request.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/sets` resource
- Use GitBash to interact with the `/sets` resource
- PATCH an existing set

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to PATCH an existing set on the service.

### 1. Understand set format

Before you PATCH a set on the BrickStack API, you must understand the
format of an existing set. Refer to the examples below.

#### For Postman

```json
  {
    "id": 30,
    "setNumber": "7000",
    "name": "Shell Gas Station",
    "theme": "City",
    "pieces": 1500,
    "minifigures": 15,
    "releaseYear": 2025,
    "ageRange": "16+",
    "price": 200,
    "retired": false,
    "tags": [
        "city",
        "store",
        "vehicles"
    ]
}
```

#### For GitBash

```shell
curl -X PATCH http://localhost:3000/sets/30/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 30,
    "setNumber": "7000",
    "name": "Shell Gas Station",
    "theme": "City",
    "pieces": 1500,
    "minifigures": 15,
    "releaseYear": 2025,
    "ageRange": "16+",
    "price": 200,
    "retired": false,
    "tags": [
      "city",
      "store",
      "vehicles"
    ]
}'
  ```

Because you are only updating partial attributes,
you do not have to enter every attribute as listed above.

### 2. Create the PATCH request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `PATCH`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/sets/30/`
4. Below the URL that you entered, click on the `Body` tab
5. Change the format to `raw`
6. Copy the set from section 1 of this document
7. Change the attributes that you want to, delete any lines that you do not want to update
8. Paste the set
9. In the top right-hand corner, click `Send`
10. Check the bottom part of the screen
11. If you have an error: correct the mistake based on the response text that you get
12. If you do not have an error: you receive a response
with the data that you just sent
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the PATCH request in GitBash

1. Open GitBash
2. Copy the GitBash command from section 1 of this document
3. Paste the command in Notepad or a similar program
4. Change / delete the attributes that you want to and copy the newly-changed set
5. Paste the GitBash command
6. Press the `enter` key
7. View the response from GitBash
8. If you have an error: correct the mistake based on the response text that you receive
9. If you do not have an error: you receive a response

### 4. View the response - Postman

You receive a response.

If you successfully patched the set, the set
appears at the bottom of the screen.
A green rectangle
with the text `200 OK` also appears.

Here is an example response:

```json
{
    "id": 30,
    "setNumber": "7000",
    "name": "Shell Gas Station",
    "theme": "City",
    "pieces": 1500,
    "minifigures": 15,
    "releaseYear": 2025,
    "ageRange": "16+",
    "price": 200,
    "retired": false,
    "tags": [
        "city",
        "store",
        "vehicles"
    ]
}
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

Here is an example response:

```json
{
  "id": 30,
  "setNumber": "7000",
  "name": "Shell Gas Station",
  "theme": "City",
  "pieces": 1500,
  "minifigures": 15,
  "releaseYear": 2025,
  "ageRange": "16+",
  "price": 200,
  "retired": false,
  "tags": [
    "city",
    "store",
    "vehicles"
  ]
}
```

If there was an error, the error text appears.

## Completion and validation

If you received a response with no errors, you have used the `PATCH` command
to partially update an existing set.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- Invalid syntax of the GitBash command
- The local server is not running

## Next steps

Now that you have used the `PATCH` command to update a set,
you can explore more of the API:

- Try posting a new set
- View other tutorials
- View the [sets API resource document](../resource/sets.md)
  