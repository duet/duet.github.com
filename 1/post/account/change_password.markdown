---
layout: default
title: POST account/change_password
---
# `{{page.title}}`

Change the password for the currently authenticated account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/change_password`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

* `account[password]`
* `account[password_confirmation]`

## Response

A JSON object containing privacy settings for the account.

### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript %}
{
    "errors" : {
        "password": [
          "doesn't match confirmation"
        ]
    }
}
{% endhighlight %}
