---
layout: default
title: POST duets/invitations/:duet_id/decline
---
# `{{page.title}}`

Decline a Duet invitation.

## URL

`{{site.api.base_url}}/{{site.api.version}}/invitations/:duet_id/decline`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

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