---
# markdownlint-disable
# vale  off
layout: default
parent: tutorials
nav_order: 3
# tags used by AI files
description: Post a `collection` to the collection resource
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites: 
    - /setup
    - /api/collection
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
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to POST a new collection to the service.

### 1. Understand collection format

Before you POST a collection to the BrickStack API, you must understand the
format of an existing collection. Refer to the examples below.

#### For Postman

```json
[
    "id": 2,
    "userId": 1,
    "setId": 17,
    "purchaseDate": "2019-12-25",
    "condition": "Built",
    "location": "Office",
    "notes": "Harry Potter collection centerpiece"
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
2. At the top of the screen in the center pane, change the HTTP method to "POST"
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/collection`
4. Below the URL that you entered, click on the `Body` tab
5. Change the format to `raw`
6. Paste the collection
7. In the top right-hand corner, click `Send`
8. Check the bottom part of the screen
9. If you have an error: correct the mistake based on the response text that you get
10. If you do not have an error: you should get a response
with the data that you just sent.
A green rectangle on the right-hand side of the screen
with the text `201 Created` is displayed.

### 3. Create the POST request in GitBash

1. Open your terminal app
2. Copy the GitBash command from section 1 of this document
3. Paste the GitBash command
4. Press the `enter` key
5. View the response from GitBash
6. If you have an error: correct the mistake based on the response text that you get
7. If you do not have an error: you will see no response.
check the instance of GitBash that is running your local server to see the response.

### 4. View the response - Postman

You will receive a response.

If you successfully posted the collection, the collection
will appear at the bottom part of the screen.
A green rectangle
with the text `201 Created` will also appear.

If there was an error, the error text will appear.

### 5. View the response - GitBash

In the local server instance of GitBash, you will receive a response.

If you successfully posted the collection, the `201` message will appear.

If there was an error, the error text will appear.

## Completion and validation

If you received a response with no errors, you have posted a collection.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- The entered user does not exist
- Invalid syntax of the GitBash command

## Next steps

Now that you have posted a collection, you can explore more of the API:

- Try posting multiple collections
- View other tutorials
- View the [collection API reference document](../api/collection.md)
  