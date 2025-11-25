---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
# tags used by AI files
description: Post a `collection` to the collection resource
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
    - POST /collection
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: Post a collection

![BrickStack Tutorial](../../images/tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `POST /collection` endpoint to post a new
LEGO collection to the BrickStack API.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/collection` resource
- Use GitBash to interact with the `/collection` resource
- POST a new collection

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application, such as GitBash

## Steps

Follow these steps to POST a new collection to the service.

### 1. Understand collection format

Before you POST a collection to the BrickStack API, you must understand the
format of an existing collection. Refer to the examples below.

#### For Postman

```json
[
  {
    "id": 2,
    "userId": 1,
    "setId": 17,
    "purchaseDate": "2019-12-25",
    "condition": "Built",
    "location": "Office",
    "notes": "Harry Potter collection centerpiece"
  }
]
```

#### For GitBash

```shell
curl -X POST http://localhost:3000/collection/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 2,
    "userId": 1,
    "setId": 17,
    "purchaseDate": "2019-12-25",
    "condition": "Built",
    "location": "Office",
    "notes": "Harry Potter collection centerpiece"
  }'
  ```

### 2. Create the POST request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `POST`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/collection/`
4. Below the URL that you entered, click on the `Body` tab
5. Change the format to `raw`
6. Copy the collection from section 1 of this document
7. Paste the collection
8. Change the attributes that you want to
9. In the top right-hand corner, click `Send`
10. Check the bottom part of the screen
11. If you have an error: correct the mistake based on the response text that you get
12. If you do not have an error: you receive a response
with the data that you just sent.
A green rectangle on the right-hand side of the screen
with the text `201 Created` displays.

### 3. Create the POST request in GitBash

1. Open GitBash
2. Copy the GitBash command from section 1 of this document
3. Paste the command in Notepad or a similar program
4. Change the attributes that you want to and copy the newly-changed collection
5. Paste the GitBash command
6. Press the `enter` key
7. View the response from GitBash
8. If you have an error: correct the mistake based on the response text that you receive
9. If you do not have an error: you receive a response

### 4. View the response - Postman

You receive a response.

If you successfully posted the collection, the collection
appears at the bottom of the screen.
A green rectangle
with the text `201 Created` also appears.

Here is an example response:

```json
{
    "id": 2,
    "userId": 1,
    "setId": 2,
    "purchaseDate": "2023-01-15",
    "condition": "Built",
    "location": "Display Room",
    "notes": "Tallest LEGO set ever made"
}
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

Here is an example response:

```json
 {
  "id": 2,
  "userId": 1,
  "setId": 17,
  "purchaseDate": "2019-12-25",
  "condition": "Built",
  "location": "Office",
  "notes": "Harry Potter collection centerpiece"
}
```

If there was an error, the error text appears.

## Completion and validation

If you received a response with no errors, you have used the `POST` command
to post a new collection.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- Invalid syntax of the GitBash command
- The local server is not running

## Next steps

Now that you have used the `POST` command to post a new collection,
you can explore more of the API:

- Try posting multiple collections
- View other tutorials
- View the [collection API resource document](../resource/collection.md)
  