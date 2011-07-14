---
layout: default
title: GET duets
---
# `{{page.title}}`

A paginated list of all duets related to the currently authenticated account.  This includes both duets proposed by the current account and duets proposed to the current account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets`

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
* `filter` - filter duets by their current state. valid options are `proposed`, `active`, and `completed`.

## Response

### `200 OK`

An array of Duet objects. See the [Duet Object documentation](/1/duet_object) for more information.
