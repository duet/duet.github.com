---
layout: default
title: POST duets/:duet_id/accept
---
# `{{page.title}}`

Accept a Duet invitation.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/accept`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Response

### `200 OK`

A Duet object. See the [Duet Object documentation](/duet_object) for more information.

### `422 Unprocessable Entity`

### `404 Not Found`
