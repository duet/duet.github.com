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

## Account Authentication Required

`false`

## Parameters

### Required

* `account[login]` - can be either `email` or `phone`
* `account[password]`

## Response

An account JSON object containing the `authentication_token` only

### HTTP Code

`200 OK` or `401 Unauthorized`

### JSON

{% highlight javascript linenos %}
{{site.api.resources.account.sign_in}}
{% endhighlight %}