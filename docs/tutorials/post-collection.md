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
- POST a new collection

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application

## Steps

Follow these steps to POST a new collection to the service.

### 1. Understand collection format

Before you POST a collection to the BrickStack API, you must understand the
format of an existing collection. Refer to the example below:

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

### 2. Create the POST request

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

### 3. View the response

You will receive a response.

If you successfully posted the collection, the collection
will appear at the bottom part of the screen.
A green rectangle
with the text `201 Created` will also appear.

If there was an error, the error text will appear.

## Completion and validation

If you received a response with no errors, you have posted a collection.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- The entered user does not exist

## Next steps

Now that you have posted a collection, you can explore more of the API:

- Try posting multiple collections
- View other tutorials
- View the [collection API reference document](../api/collection.md)
  