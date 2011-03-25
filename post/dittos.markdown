---
layout: default
title: POST dittos
---
# `{{page.title}}`

Creates a new ditto associated with the current account based on an existing duet id.

## URL

`{{site.api.base_url}}/{{site.api.version}}/dittos`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `ditto[duet_id]`

## Response

A ditto object.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.ditto.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.resources.ditto.errors}}
{% endhighlight %}
