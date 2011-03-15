---
layout: default
title: POST duets/:duet_id/update
---
# `{{page.title}}`

Update an existing duet.

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

* `duet[body]` - this can only be updated if the duet has not been accepted or decline by someone.

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

### `404 Not Found`
