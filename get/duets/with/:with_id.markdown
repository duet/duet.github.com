---
layout: default
title: GET duets/with/:with_id
---
# `{{page.title}}`

A list of the current account's duets that involve `:with_id`.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/with/:with_id`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`

## Parameters

### Optional

* `per` - default: 10
* `page` - default: 1

## Response

### `200 OK`

An array of Duet objects. See the [Duet Object documentation](/duet_object) for more information.
