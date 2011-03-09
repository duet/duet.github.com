---
layout: default
title: POST duets/:duet_id/update
---
# `{{page.title}}`

Update an existing duet.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/update`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `duet[title]`
* `duet[is_shared]` - boolean (default: 0)
* `duet[is_ditto]` - boolean (default: 0)
* `duet[privacy]` - 0: private, 1: users included, 2: my circle, 4: public

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