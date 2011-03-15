---
layout: default
title: GET duets/completed
---
# `{{page.title}}`

A list of all completed duets related to the current account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/completed`

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

An array of duet JSON objects.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.duet.collection}}
{% endhighlight %}
