---
layout: default
title: GET duets/public/featured
---
# `{{page.title}}`

Returns a list of featured duets for use in public areas of the app.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/public/featured`

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