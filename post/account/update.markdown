---
layout: default
title: POST account/update
---
# `{{page.title}}`

Update basic account information.  This does not include privacy options or the account password.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/update`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`
## Parameters

### Required

* `account[first_name]`
* `account[last_name]`
* `account[email]`
* `account[phone]`

### Optional

* `account[gender]` - acceptable values: `m`, `f`
* `account[born_on]` - format: `YYYY-MM-DD`

## Response

An account JSON object.  **Note**: You cannot update an account's password, profile image, or privacy settings from this method.  Use the respective methods available to handle those needs.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.account.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.resources.account.errors}}
{% endhighlight %}
