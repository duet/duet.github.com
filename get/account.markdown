---
layout: default
title: GET account
---
# `{{page.title}}`

Get information for an account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account`

## Format

JSON

## HTTP Method

`GET`

## Authentication Required

true

## Response

### HTTP Code

`200 OK`

### JSON

{% highlight javascript linenos %}
{
    "account" : {
      "first_name": "PJ",
      "last_name": "Kelly",
      "born_on": "1982-03-11",
      "email": "me@pjkel.ly",
      "gender": "m"
    }
}
{% endhighlight %}