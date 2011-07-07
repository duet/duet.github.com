---
layout: default
title: POST duets/:duet_id/decline
---
# `{{page.title}}`

Decline a Duet invitation.  Once you decline a duet, it will no longer appear in your account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/decline`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Optional

* `duet[declined_why]` - a message why the duet was declined.

## Response

### `200 OK`

A Duet object. See the [Duet Object documentation](/duet_object) for more information.

### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.duet.errors}}
{% endhighlight %}

### `404 Not Found`
