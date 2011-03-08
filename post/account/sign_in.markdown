---
layout: default
title: POST account/sign_in
---
# `{{page.title}}`

Get the API key for an existing account based on an email/password combination.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/sign_in`

## Format

JSON

## HTTP Method

`POST`

## Authentication Required

`false`

## Parameters

### Required

* `account[email]`
* `account[password]`

## Response

An account JSON object containing the `authentication_token` only

### HTTP Code

`200 OK` or `422 Unprocessable Entity`

### JSON

{% highlight javascript linenos %}
{
    "account" : {
      "authentication_token": "rya3yxlxLwIF2OHVJBcX2F2e7gqDGzHxmT3v7eD3E0Lu35ox8FKwzXRSQdoz"
    }
}
{% endhighlight %}