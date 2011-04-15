---
layout: default
title: POST duets/:duet_id/complete
---
# `{{page.title}}`

Mark a duet completed.  This can be done by either party involved in the duet.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/complete`

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
{
    "id": 92,
    "prefix": "Let's",
    "body": "bake a cake",
    "state": "completed",
    "proposed_by_id": 1,
    "proposed_to_id": 2
}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.resources.duet.errors}}
{% endhighlight %}

### `404 Not Found`
