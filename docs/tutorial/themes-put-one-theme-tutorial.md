---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
# tags used by AI files
description: Put a `theme` to an existing themes resource
tags:
    - api
categories: 
    - tutorials
ai_relevance: high
importance: 6
prerequisites: 
    - /setup
    - /resource/themes
related_pages: []
examples: []
api_endpoints: 
    -  PUT /themes
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: PUT an existing theme

![BrickStack Tutorial](./tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `PUT /themes` endpoint to update an existing
LEGO theme on the BrickStack API.

The `PUT` command will update a theme with the entered theme ID.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/themes` resource
- Use GitBash to interact with the `/themes` resource
- PUT an existing theme

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application, such as GitBash

## Steps

Follow these steps to PUT an existing theme on the service.

### 1. Understand theme format

Before you PUT a theme on the BrickStack API, you must understand the
format of an existing theme. Refer to the examples below.

#### For Postman

```json
  {
    "id": 7,
    "name": "Batman",
    "description": "Batman comic book character theme"
  }
```

#### For GitBash

```shell
curl -X PUT http://localhost:3000/themes/7/ \
  -H "Content-Type: application/json" \
  -d '{
    "id": 7,
    "name": "Batman",
    "description": "Batman comic book character theme"
}'
  ```

### 2. Create the PUT request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `PUT`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/themes/7/`
4. Below the URL that you entered, click on the `Body` tab
5. Change the format to `raw`
6. Copy the theme from section 1 of this document
7. Paste the theme
8. Change the attributes that you want to
9. In the top right-hand corner, click `Send`
10. Check the bottom part of the screen
11. If you have an error: correct the mistake based on the response text that you get
12. If you do not have an error: you receive a response
with the data that you just sent.
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the PUT request in GitBash

1. Open GitBash
2. Copy the GitBash command from section 1 of this document
3. Paste the command in Notepad or a similar program
4. Change the attributes that you want to and copy the newly-changed theme
5. Paste the GitBash command
6. Press the `enter` key
7. View the response from GitBash
8. If you have an error: correct the mistake based on the response text that you receive
9. If you do not have an error: you receive a response

### 4. View the response - Postman

You receive a response.

If you successfully put the theme, the theme
appears at the bottom of the screen.
A green rectangle
with the text `200 OK` also appears.

Here is an example response:

```json
{
    "id": 7,
    "name": "Batman",
    "description": "Batman comic book character theme"
}
```

If there was an error, the error text appears.

### 5. View the response - GitBash

You receive a response.

Here is an example response:

```json
{
  "id": 7,
  "name": "Batman",
  "description": "Batman comic book character theme"
}
```

If there was an error, the error text appears.

## Completion and validation

If you received a response with no errors, you have used the `PUT` command
to update an existing theme.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- Invalid syntax of the GitBash command
- The local server is not running

## Next steps

Now that you have used the `PUT` command to update a theme,
you can explore more of the API:

- Try patching an existing theme
- View other tutorials
- View the [themes API resource document](../resource/themes.md)
  