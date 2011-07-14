---
layout: default
title: POST duets/:duet_id/complete
---
# `{{page.title}}`

Mark a duet completed.  This can be done by either party involved in the duet.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/complete`

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
