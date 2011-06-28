---
layout: default
title: POST duets/:duet_id/items/:item_id/destroy
---
# `{{page.title}}`

Destroy an item associated with the duet matching `:duet_id` and the currently authenticated account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/items/:item_id/destroy`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Response

### `200 OK`

If the item was successfully destroyed.

### `422 Unprocessable Entity`

If the item could not be destroyed.

### `404 Not Found`

If the requested item or associated duet could not be found.