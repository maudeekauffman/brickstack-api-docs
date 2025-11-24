---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
# tags used by AI files
description: Post a `set` to the sets resource
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
    - POST /sets
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: Post a new set

![BrickStack Tutorial](./tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `POST /sets` endpoint to post a new
LEGO set to the BrickStack API.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/sets` resource
- Use GitBash to interact with the `/sets` resource
- POST a new set

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application, such as GitBash

## Steps

Follow these steps to POST a new set to the service.

### 1. Understand set format

Before you POST a set to the BrickStack API, you must understand the
format of an existing set. Refer to the examples below.

#### For Postman

```json
[
 {
    "id": 30,
    "setNumber": "10236",
    "name": "Texaco Gas Station",
    "theme": "City",
    "pieces": 1700,
    "minifigures": 5,
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
]
```

#### For GitBash

```shell
curl -X POST http://localhost:3000/sets/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 30,
    "setNumber": "10236",
    "name": "Texaco Gas Station",
    "theme": "City",
    "pieces": 1700,
    "minifigures": 5,
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

### 2. Create the POST request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `POST`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/sets/`
4. Below the URL that you entered, click on the `Body` tab
5. Change the format to `raw`
6. Copy the set from section 1 of this document
7. Paste the set
8. Change the attributes that you want to
9. In the top right-hand corner, click `Send`
10. Check the bottom part of the screen
11. If you have an error: correct the mistake based on the response text that you get
12. If you do not have an error: you receive a response
with the data that you just sent
A green rectangle on the right-hand side of the screen
with the text `201 Created` displays.

### 3. Create the POST request in GitBash

1. Open GitBash
2. Copy the GitBash command from section 1 of this document
3. Paste the command in Notepad or a similar program
4. Change the attributes that you want to and copy the newly-changed set
5. Paste the GitBash command
6. Press the `enter` key
7. View the response from GitBash
8. If you have an error: correct the mistake based on the response text that you receive
9. If you do not have an error: you receive a response

### 4. View the response - Postman

You receive a response.

If you successfully posted the set, the set
appears at the bottom of the screen.
A green rectangle
with the text `201 Created` also appears.

Here is an example response:

```json
[
    {
        "id": 30,
        "setNumber": "10236",
        "name": "Texaco Gas Station",
        "theme": "City",
        "pieces": 1700,
        "minifigures": 5,
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
]
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

Here is an example response:

```json
 {
  "id": 30,
  "setNumber": "10236",
  "name": "Texaco Gas Station",
  "theme": "City",
  "pieces": 1700,
  "minifigures": 5,
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

If you received a response with no errors, you have used the `POST` command
to post a new set.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- Invalid syntax of the GitBash command
- The local server is not running

## Next steps

Now that you have used the `POST` command to post a new set,
you can explore more of the API:

- Try posting multiple sets
- View other tutorials
- View the [sets API resource document](../resource/sets.md)
  