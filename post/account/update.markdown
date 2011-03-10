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
* `account[password]`
* `account[password_confirmation]`
* `account[phone]`

### Optional

* `account[gender]` - acceptable values: `m`, `f`
* `account[born_on]` - format: `YYYY-MM-DD`

## Response

### HTTP Code

`200 OK` or `422 Unprocessable Entity`

### JSON

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