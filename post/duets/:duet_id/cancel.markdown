---
layout: default
title: POST duets/:duet_id/destroy
---
# `{{page.title}}`

Destroy a duet and **all its related items**.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/destroy`

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
