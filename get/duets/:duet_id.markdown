---
layout: default
title: GET duets/:duet_id
---
# `{{page.title}}`

Get duet matching the specified `:duet_id`.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`

## Response

### `200 OK`

A Duet object. See the [Duet Object documentation](/duet_object) for more information.

### `404 Not Found`
