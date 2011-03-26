---
layout: default
title: POST duets
---
# `{{page.title}}`

Creates a new duet associated with the current account.

**Note**: Invite functionality is not in place yet. It's pending a decision on email vs. sms.

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

## Response

A duet object.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.duet.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.resources.duet.errors}}
{% endhighlight %}
