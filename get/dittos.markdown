---
layout: default
title: GET dittos
---
# `{{page.title}}`

A list of all dittos related to the current account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/dittos`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`

## Parameters

### Optional

* `num` - default: 10
* `page` - default: 1

## Response

An array of ditto JSON objects.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.dittos.collection}}
{% endhighlight %}
