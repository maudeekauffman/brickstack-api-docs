---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
# tags used by AI files
description: Get all `collections` from the collection resource
tags:
    - api
categories: 
    - tutorials
ai_relevance: high
importance: 6
prerequisites: 
    - /setup
    - /resource/collection
related_pages: []
examples: []
api_endpoints: 
    - GET /collection
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: Get all collections

![BrickStack Tutorial](../../images/tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `GET /collection` endpoint to get all
existing LEGO collections from the BrickStack API.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/collection` resource
- Use GitBash to interact with the `/collection` resource
- GET all existing collections

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to `GET` all existing collections from the service.

### 1. Understand the URL to the collection resource

Before you GET all collections from the BrickStack API, you must understand how
to call the collection resource. The link to the collection resource is:
`http://localhost:3000/collection/`.

### 2. Create the GET request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `GET`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/collection/`
4. In the top right-hand corner, click `Send`
5. Check the bottom part of the screen
6. If you have an error: correct the mistake based on the response text that you get
7. If you do not have an error: you receive a response
with with details about all collections.
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the GET request in GitBash

1. Open GitBash
2. Enter the command `curl http://localhost:3000/collection/`
3. Press the `enter` key
4. View the response from GitBash
5. If you have an error: correct the mistake based on the response text that you get
6. If you do not have an error: you receive a response with details about all collections.

### 4. View the response - Postman

You receive a response.

If you receive a response without an error, the collections
appear at the bottom part of the screen.
A green rectangle
with the text `200 OK` also appears.

Here is an example response when only 1 collection is in the API:

```json
[
    {
        "id": 3,
        "userId": 1,
        "setId": 22,
        "purchaseDate": "2018-06-10",
        "condition": "Built",
        "location": "Display Room",
        "notes": "10th anniversary modular"
    }
]
```

Here is an example response with 3 collections from the API:

```json
[
    {
        "id": 3,
        "userId": 1,
        "setId": 22,
        "purchaseDate": "2018-06-10",
        "condition": "Built",
        "location": "Display Room",
        "notes": "10th anniversary modular"
    },
    {
        "id": 4,
        "userId": 1,
        "setId": 10,
        "purchaseDate": "2022-08-20",
        "condition": "Built",
        "location": "Display Room",
        "notes": "Part of modular collection"
    },
    {
        "id": 5,
        "userId": 1,
        "setId": 14,
        "purchaseDate": "2020-10-15",
        "condition": "Built",
        "location": "Display Room",
        "notes": "Perfect for Halloween display"
    }
]
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

If you receive a response without an error, details about all collections
appear.

Here is an example response when only 1 collection is in the API:

```json
{
  "id": 1,
  "userId": 1,
  "setId": 2,
  "purchaseDate": "2023-01-15",
  "condition": "Built",
  "location": "Display Room",
  "notes": "Tallest LEGO set ever made"
}
```

Here is an example response with 3 collections from the API:

```json
[
    {
        "id": 3,
        "userId": 1,
        "setId": 22,
        "purchaseDate": "2018-06-10",
        "condition": "Built",
        "location": "Display Room",
        "notes": "10th anniversary modular"
    },
    {
        "id": 4,
        "userId": 1,
        "setId": 10,
        "purchaseDate": "2022-08-20",
        "condition": "Built",
        "location": "Display Room",
        "notes": "Part of modular collection"
    },
    {
        "id": 5,
        "userId": 1,
        "setId": 14,
        "purchaseDate": "2020-10-15",
        "condition": "Built",
        "location": "Display Room",
        "notes": "Perfect for Halloween display"
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

Now that you have used `GET` to get all existing collections,
you can explore more of the API:

- Try getting one collection
- View other tutorials
- View the [collection API resource document](../resource/collection.md)
  