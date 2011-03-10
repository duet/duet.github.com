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

## Account Authentication Required

`true`

## Response

An account JSON object.

### `200 OK`

{% highlight javascript linenos %}
{
  "account" : {
    "gender": null,
    "phone": "12121234567",
    "last_name": "Towne",
    "email": "account-5@email.com",
    "first_name": "Blaise",
    "born_on": null
  }
}
{% endhighlight %}