---
layout: default
title: POST duets/:duet_id/reopen
---
# `{{page.title}}`

Reopen a duet that has been completed.  This can be done by either party involved in the duet.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/reopen`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Response

### `200 OK`

A Duet object. See the [Duet Object documentation](/1/duet_object) for more information.

### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.duet.errors}}
{% endhighlight %}

### `404 Not Found`
