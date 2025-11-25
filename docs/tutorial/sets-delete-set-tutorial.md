---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
# tags used by AI files
description: Delete an existing `sets` resource
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
    -  DELETE /sets
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Tutorial: DELETE an existing set

![BrickStack Tutorial](../../tutorial.png "BrickStack Tutorial")

Use this tutorial to use the `DELETE /sets` endpoint to delete an existing
LEGO set from the BrickStack API.

The `DELETE` command will delete a set with the entered set ID.

**Estimated time:** 15 minutes

## Goal

After you complete this tutorial, you can:

- Use Postman to interact with the `/sets` resource
- Use GitBash to interact with the `/sets` resource
- DELETE an existing set

## Prerequisites

Before you start, ensure that you have completed the initial setup.

- **Required**: [Setup](../setup.md).
- Your local server must be running. If it's not, run `json-server -w db.json`
from the main directory
- The base URL for your local service is `http://localhost:3000`
- You must use the Postman application or a terminal application such as GitBash

## Steps

Follow these steps to DELETE a set from the service.

### 1. Understand the URL to the set resource

Before you DELETE a set from the BrickStack API, you must understand how
to call the sets resource. The link to a specific set is:
`http://localhost:3000/sets/1/` This link makes a request
to delete the set with the ID `1`.

### 2. Create the DELETE request in PostMan

1. Open PostMan
2. At the top of the screen in the center pane, change the HTTP method to `DELETE`
3. To the right of the HTTP method,
   enter the URL as `http://localhost:3000/sets/1/`
4. In the top right-hand corner, click `Send`
5. Check the bottom part of the screen
6. If you have an error: correct the mistake based on the response text that you get
7. If you do not have an error: you receive a response with `{}` displayed
A green rectangle on the right-hand side of the screen
with the text `200 OK` displays.

### 3. Create the DELETE request in GitBash

1. Open GitBash
2. Enter the command `curl -X DELETE http://localhost:3000/sets/1/`
3. Press the `enter` key
4. View the response from GitBash
5. If you have an error: correct the mistake based on the response text that you get
6. If you do not have an error: you receive a response with details about the set

### 4. View the response - Postman

You receive a response.

If you successfully deleted the set, `{}`
appears at the bottom of the screen.
A green rectangle
with the text `200 OK` also appears.

If there was an error, the error text appears.

### 5. View the response - GitBash

The response displays on the instance of the terminal that is running the server:

```shell
DELETE /sets/1/ 200 27.533 ms - 2
```

If there was an error, the error text appears.

## Completion and validation

If you received a response with no errors, you have used the `DELETE` command
to delete an existing set.

If you received an error, read the text of the error. Errors might be due to:

- Invalid formatting, for example missing `[]` or `{}` symbols
- Invalid syntax of the GitBash command
- The local server is not running

## Next steps

Now that you have used the `DELETE` command on an existing set,
you can explore more of the API:

- Try posting a new set
- View other tutorials
- View the [sets API resource document](../resource/sets.md)
  