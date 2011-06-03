---
layout: default
title: GET duets/:duet_id/items
---
# `{{page.title}}`

Get all items for the duet matching the specified `:duet_id`.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/items`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`

## Response

A collection of item objects.  There are three types of item objects: `message`, `image`, and `video`.  In the json objects returned those nodes may or may not exist depending on the type of item it is.  In the case of `video` objects, they will have both a `video` and `image` key, the `image` being a screencap from the video.

### `200 OK`

{% highlight javascript linenos %}
{{site.api.resources.item.collection}}
{% endhighlight %}

### `404 Not Found`
