---
# markdownlint-disable
# vale  off
layout: default
nav_order: 2
parent: Resource docs
# tags used by AI files
description: "Information about the `sets` resource"
tags: 
    - api
categories: 
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/sets
examples: []
api_endpoints:
    - /sets
version: "v1.0"
last_updated: "2025-11-08"
# vale  on
# markdownlint-enable
---

# `sets` resource

![BrickStack Resource](../images/resource.png "BrickStack Resource")

Base endpoint:

```shell
{server_url}/sets
```

Contains information about available LEGO sets in the BrickStack API.

## Resource properties

Sample `sets` resource

```js

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
      "tags": ["architecture", "landmark", "paris", "record breaker"]
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The ID of the LEGO set |
| `setNumber` | number | The LEGO ID for the LEGO set |
| `name` | string | The English name of the LEGO set |
| `theme` | string | The general theme of the LEGO set |
| `pieces` | number | The number of pieces of the LEGO set |
| `minifigures` | number | The number of LEGO people that are included in the LEGO set |
| `ageRange` | string | The recommended age for use of the LEGO set |
| `price` | string | The cost of the LEGO set in USD currency |
| `retired` | boolean | If the LEGO set has been retired from circulation |
| `tags` | array | Associated tags of the LEGO resource, more than one can be used |

## READ

* [Browse all sets](../tutorial/sets-get-all-sets-tutorial.md)
* [Search a specific set](../tutorial/sets-get-one-set-tutorial.md)
