---
layout: default
title: GET duets/with/:second_account_id
---
# `{{page.title}}`

A list of the current user's duets that involve `:second_account_id`.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/with/:second_account_id`

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