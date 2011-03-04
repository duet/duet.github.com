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

## Authentication Required

true

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
      "first_name": "PJ",
      "last_name": "Kelly",
      "born_on": "1982-03-11",
      "email": "me@pjkel.ly",
      "phone": "5625050434",
      "gender": "m"
    }
}
{% endhighlight %}