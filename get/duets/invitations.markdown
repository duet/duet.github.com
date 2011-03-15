---
layout: default
title: GET duets/invitations
---
# `{{page.title}}`

Returns a list of duets you have been invited to.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/invitations`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`

## Parameters

### Optional

* `num` - default: 10
* `page` - default: 1

## Response

An array of duet JSON objects.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.duet.collection}}
{% endhighlight %}
