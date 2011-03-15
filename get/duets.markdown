---
layout: default
title: GET duets
---
# `{{page.title}}`

Get duets for the currently authenticated account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets`

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
