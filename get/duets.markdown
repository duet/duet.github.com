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