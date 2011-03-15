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

## Response

An array of duet JSON objects.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.duet.collection}}
{% endhighlight %}
