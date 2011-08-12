---
layout: default
title: POST duets/:duet_id/items
---
# `{{page.title}}`

Creates a new item associated with the duet matching `:duet_id` and the currently authenticated account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/items`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `item[message]` - limit 100 characters.  Required **only** if image and video are not included.

### Optional

* `item[image]` - either an image if no video is being sent or a screencap to accompany the video being sent
* `item[video]` - a video in m4v format

## Response

An item object.

### `200 OK`

{% highlight javascript %}
{{site.api.resources.item.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.item.errors}}
{% endhighlight %}
