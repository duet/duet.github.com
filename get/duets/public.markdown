---
layout: default
title: GET duets/public
---
# `{{page.title}}`

Returns a list of publicly available duets for use in public areas of the app in reverse-chronological order.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/public`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`false`

## Parameters

### Optional

* `num` - default: 10
* `page` - default: 1

## Response

An array of duet JSON objects with sensitive data omitted.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.duet.public_collection}}
{% endhighlight %}
