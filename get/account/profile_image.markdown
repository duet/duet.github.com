---
layout: default
title: GET account/profile_image
---
# `{{page.title}}`

Get the profile photo for an existing account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/profile_image`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`
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