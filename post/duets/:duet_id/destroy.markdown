---
layout: default
title: POST duets/:duet_id/destroy
---
# `{{page.title}}`

Destroy a duet and **all its related items**.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/destroy`

## Format

JSON

## HTTP Method

`POST`

## Authentication Required

`true`

## Response

A duet object.

### HTTP Code

`200 OK` or `422 Unprocessable Entity`

### JSON

{% highlight javascript linenos %}
{
    "duet" : {
      "id": 34,
      "title": "Make a pie.",
      "is_shared": false,
      "is_ditto": false,
      "privacy": 2
    }
}
{% endhighlight %}