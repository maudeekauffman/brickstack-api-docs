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

# Overview of the BrickStack API

![BrickStack API logo](./images/brickstack_api.png "BrickStack API logo")

Welcome to `BrickStack!` BrickStack is an API that stores information about LEGO sets.

This API is fictional and is not a real service.

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

This document shows you how to use the `get` command to retrieve
all sets or only 1 sets. Use the document to get a better
understanding of what BrickStack does.

## Tutorials

Learn how to do common tasks with BrickStack. These documents
show you a step-by-step process about how to interact
with the BrickStack API.

First, read this setup guide to set up your development system for
these tutorials. You only have to do this process one time per
development system.

* [Setup](./setup.md)

After your system is ready, read these tutorials to learn how to perform common tasks in BrickStack.

* [Get all sets](./tutorial/sets-get-all-sets-tutorial.md)
* [Update an existing set](./tutorial/sets-put-one-set-tutorial.md)
* [Add a new set](./tutorial/sets-post-new-set-tutorial.md)
* [Get a specific collection (your collection, for example)](./tutorial/collection-get-one-collection-tutorial.md)

## API Reference docs

At-a-glance documents that describe how to interact with
the BrickStack API. These documents are not as detailed
as the tutorial documents. Use the Reference docs to find
something quickly.

[Click here to read the reference documents.](./reference.md)

## API Resource docs

Descriptions of the resources for the BrickStack API.

Read these documents to get an idea of what the resources of the API
are. These documents are a quick read, and the content is not as
in-depth as a tutorial.

The API resource docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
usually `http://localhost:3000`.

* [sets resource](./resource/sets.md)
* [collection resource](./resource/collection.md)
* [themes resource](./resource/themes.md)
* [users resource](./resource/users.md)
