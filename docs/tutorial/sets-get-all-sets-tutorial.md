---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
# tags used by AI files
description: Get all `sets` from the sets resource
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
    - GET /sets
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: Get all sets

![BrickStack Tutorial](./tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `GET /sets` endpoint to get all
existing LEGO sets from the BrickStack API.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/sets` resource
- Use GitBash to interact with the `/sets` resource
- GET all existing sets

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to `GET` all existing sets from the service.

### 1. Understand the URL to the sets resource

Before you GET all sets from the BrickStack API, you must understand how
to call the sets resource. The link to the sets resource is:
`http://localhost:3000/sets/`.

### 2. Create the GET request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `GET`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/sets/`
4. In the top right-hand corner, click `Send`
5. Check the bottom part of the screen
6. If you have an error: correct the mistake based on the response text that you get
7. If you do not have an error: you receive a response
with with details about all sets.
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the GET request in GitBash

1. Open GitBash
2. Enter the command `curl http://localhost:3000/sets/`
3. Press the `enter` key
4. View the response from GitBash
5. If you have an error: correct the mistake based on the response text that you get
6. If you do not have an error: you receive a response with details about all sets

### 4. View the response - Postman

You receive a response.

If you receive a response without an error, the sets
appear at the bottom part of the screen.
A green rectangle
with the text `200 OK` also appears.

Here is an example response when only 1 set is in the API:

```json
{
    "id": 1,
    "setNumber": "10234",
    "name": "Sydney Opera House",
    "theme": "Creator Expert",
    "pieces": 1929,
    "minifigures": 0,
    "releaseYear": 2013,
    "ageRange": "16+",
    "price": 324.99,
    "retired": true,
    "tags": [
        "architecture",
        "landmark",
        "australia"
    ]
}
```

Here is an example response with 3 sets from the API:

```json
[
    {
        "id": 1,
        "setNumber": "10234",
        "name": "Sydney Opera House",
        "theme": "Creator Expert",
        "pieces": 1929,
        "minifigures": 0,
        "releaseYear": 2013,
        "ageRange": "16+",
        "price": 324.99,
        "retired": true,
        "tags": [
            "architecture",
            "landmark",
            "australia"
        ]
    },
    {
        "id": 2,
        "setNumber": "10307",
        "name": "Eiffel Tower",
        "theme": "Icons",
        "pieces": 10001,
        "minifigures": 0,
        "releaseYear": 2022,
        "ageRange": "18+",
        "price": 629.99,
        "retired": false,
        "tags": [
            "architecture",
            "landmark",
            "paris",
            "record breaker"
        ]
    },
    {
        "id": 3,
        "setNumber": "21061",
        "name": "Notre-Dame de Paris",
        "theme": "Architecture",
        "pieces": 4383,
        "minifigures": 0,
        "releaseYear": 2021,
        "ageRange": "18+",
        "price": 229.99,
        "retired": false,
        "tags": [
            "architecture",
            "cathedral",
            "paris",
            "historical"
        ]
    }
]
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

If you receive a response without an error, details about all sets
appear.

Here is an example response when only 1 set is in the API:

```json
{
  "id": 1,
  "setNumber": "10234",
  "name": "Sydney Opera House",
  "theme": "Creator Expert",
  "pieces": 1929,
  "minifigures": 0,
  "releaseYear": 2013,
  "ageRange": "16+",
  "price": 324.99,
  "retired": true,
  "tags": [
    "architecture",
    "landmark",
    "australia"
  ]
}
```

Here is an example response with 3 sets from the API:

```json
[
    {
    "id": 1,
    "setNumber": "10234",
    "name": "Sydney Opera House",
    "theme": "Creator Expert",
    "pieces": 1929,
    "minifigures": 0,
    "releaseYear": 2013,
    "ageRange": "16+",
    "price": 324.99,
    "retired": true,
    "tags": [
      "architecture",
      "landmark",
      "australia"
    ]
  },
  {
    "id": 2,
    "setNumber": "10307",
    "name": "Eiffel Tower",
    "theme": "Icons",
    "pieces": 10001,
    "minifigures": 0,
    "releaseYear": 2022,
    "ageRange": "18+",
    "price": 629.99,
    "retired": false,
    "tags": [
      "architecture",
      "landmark",
      "paris",
      "record breaker"
    ]
  },
  {
    "id": 3,
    "setNumber": "21061",
    "name": "Notre-Dame de Paris",
    "theme": "Architecture",
    "pieces": 4383,
    "minifigures": 0,
    "releaseYear": 2021,
    "ageRange": "18+",
    "price": 229.99,
    "retired": false,
    "tags": [
      "architecture",
      "cathedral",
      "paris",
      "historical"
    ]
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

Now that you have used `GET` to get all existing sets,
you can explore more of the API:

- Try getting one set
- View other tutorials
- View the [sets API resource document](../resource/sets.md)
  