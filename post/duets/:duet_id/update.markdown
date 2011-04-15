---
layout: default
title: POST duets/:duet_id/update
---
# `{{page.title}}`

Update an existing duet's body attribute.  This can only be done if the duet is still in the unpaired state.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/update`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `duet[body]`

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
