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

## Authentication Required

`false`

## Parameters

### Optional

* `num` - default: 10
* `page` - default: 1

## Response

An array of duet JSON objects.

### HTTP Code

`200 OK`

### JSON

{% highlight javascript linenos %}
{
  "duets" : [
    {
      "id": 1
    },
    {
      "id": 2
    }
  ]
}
{% endhighlight %}