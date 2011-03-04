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

An array of account JSON objects.

### HTTP Code

`200 OK`

### JSON

{% highlight javascript linenos %}
{
  "accounts" : [
    {
      "first_name": "PJ",
      "last_name": "Kelly",
      "born_on": "1982-03-11",
      "email": "me@pjkel.ly",
      "gender": "m"
    },
    {
      "first_name": "Nathan",
      "last_name": "Heleine",
      "born_on": "1981-08-13",
      "email": "nathan@crushlovely.com",
      "gender": "m"
    }
  ]
}
{% endhighlight %}