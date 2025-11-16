---
# markdownlint-disable
# vale  off
layout: default
nav_order: 4
has_children: true
has_toc: false
# tags used by AI files
description: "Information about the `themes` resource"
tags: 
    - api
categories: 
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/themes
examples: []
api_endpoints:
    - /themes
version: "v1.0"
last_updated: "2025-11-08"
# vale  on
# markdownlint-enable
---

# `themes` resource

![BrickStack Resource](../images/resource.png "BrickStack Resource")

Base endpoint:

```shell
{server_url}/themes
```

Contains information about LEGO set themes / series for the BrickStack API.

## Resource properties

Sample `themes` resource

```js
{
      "id": 4,
      "name": "Architecture",
      "description": "Architectural landmarks and buildings"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The ID of the theme resource |
| `name` | string | The name of the theme for the LEGO set |
| `description` | number | The description of the LEGO set theme |

## READ

- [`themes` resource](#themes-resource)
  - [Resource properties](#resource-properties)
  - [READ](#read)
