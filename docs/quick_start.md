---
# markdownlint-disable
# vale  off
layout: default
nav_order: 3
# tags used by AI files
description: Describes how to get started using the BrickStack API for a new user
tags: 
    - quick start
categories: 
    - quick start
ai_relevance: high
importance: 9
prerequisites: []
related_pages: 
    - /setup
    - /tutorials/get-all-sets
    - /tutorials/get-one-set
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2025-11-08"
# vale  on
# markdownlint-enable
---

# Quick Start Get Sets

## Introduction

![BrickStack Quick Start](./images/quick_start.png "BrickStack Quick Start")

This document helps you to understand how to use the GET method to
interact with sets on the BrickStack API.

By reading this Quick Start guide, you should be able to understand
and use the GET method.

You will use the GET method to retrieve a list of all sets
and a specific set using the API.

Use the HTTP method "GET" to request data in REST APIs
from a specific resource.

For more details on the GET method, [see this page.](https://www.w3schools.com/tags/ref_httpmethods.asp)

Allow 15 minutes for successfully reading and understanding this document.

Before you start the document, please [read the setup guide here.](./setup.md)

## Retrieve a list of all sets

### Use cURL (all sets)

Using Git Bash or another terminal application, enter the following text:

```shell
curl http://localhost:3000/sets/
```

Use the GET method to query the sets resource for a list of all the sets.

You will receive a list of all the sets as a response in Git Bash.

The result will look something like this:

```json
[
    {
        "id": 1,
        "setNumber": "10234",
        "name": "Sydney Opera House",
        "theme": "Creator Expert",
        "pieces": 1929,
        "minifigures": 0,
        "releaseYear": 2013,
        "ageRange": "16+",
        "price": 324.99,
        "retired": true,
        "tags": [
            "architecture",
            "landmark",
            "australia"
        ]
    },
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
        "tags": [
            "architecture",
            "landmark",
            "paris",
            "record breaker"
        ]
    },
    {
        "id": 3,
        "setNumber": "21061",
        "name": "Notre-Dame de Paris",
        "theme": "Architecture",
        "pieces": 4383,
        "minifigures": 0,
        "releaseYear": 2021,
        "ageRange": "18+",
        "price": 229.99,
        "retired": false,
        "tags": [
            "architecture",
            "cathedral",
            "paris",
            "historical"
        ]
    }
]
```

If you do not receive a response at all, ensure that your local JSON server is running.

### Use Postman (all sets)

 Make sure that you select the "GET" method from the drop-down menu in the bar
 at the top of the screen.

 Enter the following text.

```shell
http://localhost:3000/sets/
```

Use the GET method to query the sets resource for
a list of all the sets.

You will receive a list of all the sets as a response in the "Body" tab
at the bottom of Postman.

The result should look something like this:

```json
[
    {
    "id": 1,
    "setNumber": "10234",
    "name": "Sydney Opera House",
    "theme": "Creator Expert",
    "pieces": 1929,
    "minifigures": 0,
    "releaseYear": 2013,
    "ageRange": "16+",
    "price": 324.99,
    "retired": true,
    "tags": [
      "architecture",
      "landmark",
      "australia"
    ]
  },
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
    "tags": [
      "architecture",
      "landmark",
      "paris",
      "record breaker"
    ]
  },
  {
    "id": 3,
    "setNumber": "21061",
    "name": "Notre-Dame de Paris",
    "theme": "Architecture",
    "pieces": 4383,
    "minifigures": 0,
    "releaseYear": 2021,
    "ageRange": "18+",
    "price": 229.99,
    "retired": false,
    "tags": [
      "architecture",
      "cathedral",
      "paris",
      "historical"
    ]
  }
]
```

If you do not receive a response at all, ensure that your local JSON server is running.

## Retrieve 1 specific set

### Use cURL (1 set)

Using Git Bash or another terminal application, enter the following text:

```shell
curl http://localhost:3000/sets/1/
```

Use the GET method to query the sets resource for one specific set.

You will receive a result response in Git Bash.

The result should look something like this:

```json
{
    "id": 1,
    "setNumber": "10234",
    "name": "Sydney Opera House",
    "theme": "Creator Expert",
    "pieces": 1929,
    "minifigures": 0,
    "releaseYear": 2013,
    "ageRange": "16+",
    "price": 324.99,
    "retired": true,
    "tags": [
      "architecture",
      "landmark",
      "australia"
    ]
}
```

Change the number in your query to get a different set.

If you do not receive a response at all, there might not be a
set with the number that you enter.

If you cannot retrieve any sets, ensure that your
local JSON server is running.

### Use Postman (1 set)

 Make sure that you select the "GET" method from the drop-down menu
 in the bar at the top of the screen.

 Enter the following text.

```shell
http://localhost:3000/sets/1/
```

Use the GET method to query the sets resource for one specific set.

You will receive the retrieved result in the "Body" tab at the bottom of Postman.

The result should look something like this:

```json
{
    "id": 1,
    "setNumber": "10234",
    "name": "Sydney Opera House",
    "theme": "Creator Expert",
    "pieces": 1929,
    "minifigures": 0,
    "releaseYear": 2013,
    "ageRange": "16+",
    "price": 324.99,
    "retired": true,
    "tags": [
      "architecture",
      "landmark",
      "australia"
    ]
}
```

Change the number in your query to get a different set.

If you do not receive a response at all, there might not be a set with the number
that you enter.

If you cannot retrieve any sets, ensure that your local JSON server is running.

## Conclusion

In this guide, you have successfully learned how to use the GET method to
query a full list of sets.

You have also learned how to GET a specific set using both cURL and Postman.

## Next steps

If you want more information about the BrickStack API, visit these related topics.

* [To-Do Service API Overview](./index.md)
* [Post a new set](./tutorials/sets-post-new-set-tutorial.md)
* [Delete a set](./tutorials/sets-delete-set-tutorial.md)
