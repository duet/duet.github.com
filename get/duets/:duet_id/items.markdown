---
layout: default
title: GET duets/:duet_id/items
---
# `{{page.title}}`

Get all items for the duet matching the specified `:duet_id`.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/items`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`

## Response

A collection of item objects.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.duet.basic}}
{% endhighlight %}

### `404 Not Found`
