---
layout: default
title: GET account/circle
---
# `{{page.title}}`

A paginated list of accounts the authenticated account is connected to.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/circle`

## Format

JSON

## HTTP Method

`GET`

## Authentication Required

true

## Parameters

### Optional

* `num` - default: 10
* `page` - default: 1

## Response

### HTTP Code

`200 OK`

### JSON

{% highlight javascript linenos %}
{
  [
    "account" : {
      "photo": "http://cdn.duet.me/path/to/image/jpg"
    }
  ]
}
{% endhighlight %}