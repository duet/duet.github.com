---
layout: default
title: POST account/image
---
# `{{page.title}}`

Set a profile photo for an existing account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/image`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `account[image]` - file upload in png, jpg, or gif format

## Response

An account JSON object.

### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript %}
{
    "errors" : {
        "image": ["is not an allowed file type"]
    }
}
{% endhighlight %}
