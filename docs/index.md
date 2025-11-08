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
    - /before-you-start-a-tutorial 
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

An image will be inserted here.

Welcome to BrickStack! BrickStack is an API that stores information about LEGO sets.

BrickStack will let you browse LEGO sets in a database to view more details about a specific LEGO set.

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

A diagram will be inserted here.

## Quickstart

[Browse all sets _(coming soon)_](#quickstart) - Use this guide to see how
easy and fun BrickStack is to use!

## Tutorials

Learn how to do common tasks with BrickStack

First, do this tutorial to set up your development system for these tutorials.
You only have to do this one time per development system.

* [setup](setup.md)

After your system is ready, these tutorials show you how to perform common tasks in BrickStack.

* [Browse all sets](tutorials/enroll-a-new-user.md)
* [Update an existing set](tutorials/add-a-new-task.md)
* [Add a set _(coming soon)_](#tutorials)
* [View your collection _(coming soon)_](#tutorials)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
usually `http://localhost:3000`.

* [sets resource](api/sets.md)
* [themes resource](api/themes.md)
* [collection resource](api/collection.md)
