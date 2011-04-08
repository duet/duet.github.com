---
layout: default
title: POST duets/invitations/:id/accept
---
# `{{page.title}}`

Accept a Duet invitation.

## URL

`{{site.api.base_url}}/{{site.api.version}}/invitations/:id/accept`

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
{{site.resources.duet.basic}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.resources.duet.errors}}
{% endhighlight %}

### `404 Not Found`
