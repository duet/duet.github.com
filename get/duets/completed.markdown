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