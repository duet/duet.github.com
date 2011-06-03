---
layout: default
title: POST duets
---
# `{{page.title}}`

Creates a new duet with the current account as the proposer.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `duet[body]` - limit 100 characters

### Optional

* `duet[video]` - a video in m4v format

## Response

A duet object.

### `200 OK`

{% highlight javascript linenos %}
{{site.api.resources.duet.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.api.resources.duet.errors}}
{% endhighlight %}
