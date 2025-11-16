---
# markdownlint-disable
# vale  off
layout: default
nav_order: 1
# tags used by AI files
description: Describes the BrickStack Service for a new user
tags: 
    - introduction
categories: 
    - introduction
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

# BrickStack API

![BrickStack API logo](./images/brickstack_api.png "BrickStack API logo")

Welcome to `BrickStack!` BrickStack is an API that stores information about LEGO sets.

Use BrickStack to browse LEGO sets in a database to view more details about a specific LEGO set.

You can browse by many attributes to help you find the right set for you.

Some examples are:

* Piece count
* Release year
* Price range
* Theme

If you notice anything incorrect or missing in the API for the existing LEGO sets,
you can either update an existing set or add a new set.

You can also start a collection to help keep track of your own LEGO sets.

## Workflow

Here is how the BrickStack API works.

![BrickStack API architecture diagram](./images/api_architecture_diagram.png "BrickStack API architecture diagram")

You use a terminal app like Git Bash or Postman. With your local json server installed,
you send a request to the BrickStack API. You are interacting with 1 of the 4 resources
that are available on the API. The request that you make modifies the json database.

## Quick Start

[Browse all sets](./quick_start.md) - Use this guide to see how
easy and fun BrickStack is to use!

## Tutorials

Learn how to do common tasks with BrickStack

First, read this tutorial to set up your development system for these tutorials.
You only have to do this process one time per development system.

* [Setup](./setup.md)

After your system is ready, read these tutorials to learn how to perform common tasks in BrickStack.

* [Get all sets](./tutorials/sets-get-all-sets-tutorial.md)
* [Update an existing set](./tutorials/sets-put-one-set-tutorial.md)
* [Add a new set](./tutorials/sets-post-new-set-tutorial.md)
* [Get a specific collection (your collection, for example)](./tutorials/collection-get-one-collection-tutorial.md)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
usually `http://localhost:3000`.

* [sets resource](./api/sets.md)
* [collection resource](./api/collection.md)
* [themes resource](./api/themes.md)
* [users resource](./api/users.md)
