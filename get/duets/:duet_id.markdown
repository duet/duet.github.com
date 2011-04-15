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

A duet object.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.duet.basic}}
{% endhighlight %}

### `404 Not Found`
