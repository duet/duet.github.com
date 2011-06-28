---
layout: default
title: POST duets/:duet_id/cancel
---
# `{{page.title}}`

Cancel a duet.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/cancel`

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

{% highlight javascript linenos %}
{{site.api.resources.duet.errors}}
{% endhighlight %}

### `404 Not Found`
