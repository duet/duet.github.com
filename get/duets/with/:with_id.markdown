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

## Parameters

### Optional

* `per` - default: 10
* `page` - default: 1

## Response

An array of duet JSON objects.

### HTTP Code

`200 OK`

### JSON

{% highlight javascript linenos %}
{{site.resources.duet.collection}}
{% endhighlight %}