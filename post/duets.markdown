---
layout: default
title: POST duets
---
# `{{page.title}}`

Creates a new duet associated with the current account.

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

* `duet[body]`

### Optional

* `duet[with_id]` - the account id of the person you're inviting

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
