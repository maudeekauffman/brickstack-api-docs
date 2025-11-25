---
# markdownlint-disable
# vale  off
layout: default
nav_order: 1
parent: Resource docs
# tags used by AI files
description: "Information about the `collection` resource"
tags: 
    - api
categories: 
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/collection
examples: []
api_endpoints:
    - /collection
version: "v1.0"
last_updated: "2025-11-08"
# vale  on
# markdownlint-enable
---

# `collection` resource

![BrickStack Resource](../../resource.png "BrickStack Resource")

Base endpoint:

```shell
{server_url}/collection
```

Contains information about personal LEGO collections for users on the BrickStack API.

## Resource properties

Sample `collection` resource

```js

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

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The ID of the collection resource |
| `userId` | number | The user ID that the collection belongs to |
| `setId` | number | The ID of the LEGO set |
| `purchaseDate` | string | The date that the collection was bought, in YYYY-MM-DD format |
| `condition` | string | The physical condition the collection is in |
| `location` | string | The physical location that the collection is stored at |
| `notes` | string | Notes entered about the collection |

## READ

* [Get all collections](../tutorial/collection-get-all-collections-tutorial.md)
* [Get collection by collection ID](../tutorial/collection-get-one-collection-tutorial.md)
