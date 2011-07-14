---
layout: default
title: POST duets/:duet_id/cancel
---
# `{{page.title}}`

Cancel a duet.  Once you cancel a duet, it will no longer appear in your account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/cancel`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Optional

* `duet[canceled_why]` - a message why the duet was canceled.

## Response

### `200 OK`

A Duet object. See the [Duet Object documentation](/1/duet_object) for more information.

### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.duet.errors}}
{% endhighlight %}

### `404 Not Found`
