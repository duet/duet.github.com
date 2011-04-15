---
layout: default
title: POST duets/:duet_id/decline
---
# `{{page.title}}`

Decline a Duet invitation.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/decline`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Response

A duet object.

### `200 OK`

{% highlight javascript linenos %}
{
    "id": 92,
    "prefix": "Let's",
    "body": "bake a cake",
    "state": "declined",
    "proposed_by_id": 1,
    "proposed_to_id": 2
}
{% endhighlight %}

### `422 Unprocessable Entity`

### `404 Not Found`
