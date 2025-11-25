---
# markdownlint-disable
# vale  off
layout: default
nav_order: 3
parent: Resource docs
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

![BrickStack Resource](../../images/resource.png "BrickStack Resource")

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

* [Browse all themes](../tutorial/themes-get-all-themes-tutorial.md)
* [Search a specific theme](../tutorial/themes-get-one-theme-tutorial.md)
