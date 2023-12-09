---
weight: 10
title: Introduction
---

# Introduction

Welcome to the Cosmos API documentation! [Cosmos](https://github.com/bbengfort/cosmos) is an expansive, API-driven game of starships and planets. The primary goal of the game is that it is entirely API-driven: all of the game logic and behaviors are captured via turn-based queries to the API. Although a lightweight web front-end exists, I'm hoping that we can collaborate on the game together either by:

1. Creating game playing AIs that use the API to play
2. Creating rich front-ends with better graphics and animation
3. Enriching the game rules by contributing to the open source API
4. Creating tournaments or other game events

The event horizon is the limit! Whatever we can think of, we should do!

# API Usage

> Requests must have the following headers:

```
GET /v1/status HTTP/1.1
Host: api.cosmosgame.space
Accept: application/json
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en
Content-Type: application/json
```

The Cosmos API is a primarily a [REST API](https://www.redhat.com/en/topics/api/what-is-a-rest-api) whose data format is JSON. All requests must have the `Content-Type` and `Accept` headers set to `application/json` and responses should be decoded using a JSON parser.

Production requests should be sent to: `https://api.cosmosgame.space`.

If you're developing locally, send requests to `http://127.0.0.1:8888`.

It's also good practice to add a `User-Agent` header, particularly if you've developed code that is interacting with the API. The value of the user agent header is generally in the form `<product> / <product-version> <comment>`; for example if I created a Python client called `pycosmos` then my user agent would be `pycosmos/1.0.0`. [Semantic versioning](https://semver.org/) is preferred to make version parsing simpler.