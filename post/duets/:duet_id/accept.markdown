---
layout: default
title: POST duets/:duet_id/accept
---
# `{{page.title}}`

Accept a Duet invitation.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/accept`

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
{{site.api.resources.duet.active}}
{% endhighlight %}

### `422 Unprocessable Entity`

### `404 Not Found`
