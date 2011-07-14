---
layout: default
title: POST account
---
# `{{page.title}}`

Creates a new duet account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`false`

## Parameters

### Required

* `account[first_name]`
* `account[last_name]`
* `account[email]`
* `account[password]`
* `account[phone]`

### Optional

* `account[gender]` - acceptable values: `m`, `f`
* `account[born_on]` - format: `YYYY-MM-DD` (no time included)

## Response

An account JSON object.  **Note**: If you want to sign the account in immediately after successfully creating it, an immediate call to [`POST account/sign_in`](/1/post/account/sign_in) should be made so the `authentication_token` can be retrieved.

### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.account.errors}}
{% endhighlight %}
