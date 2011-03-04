---
layout: default
title: POST account/profile_image
---
# `{{page.title}}`

Set a profile photo for an existing account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/profile_image`

## Format

JSON

## HTTP Method

`POST`

## Authentication Required

true

## Parameters

### Required

* `account[photo]` - file upload

## Response

### HTTP Code

`200 OK` or `422 Unprocessable Entity`

### JSON

{% highlight javascript linenos %}
{
    "account" : {
      "photo": "http://cdn.duet.me/path/to/image/jpg"
    }
}
{% endhighlight %}