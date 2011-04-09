---
layout: default
title: POST duets/:id/propose
---
# `{{page.title}}`

Propose a duet to either an account in your circle or a phone number.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:id/propose`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `duet[propose_to]` - `id` of account in your circle or phone number of person that isn't in your circle you want to propose this duet to.

## Response

A duet object.

### `200 OK`

{% highlight javascript linenos %}
{
    "id": 92,
    "prefix": "Let's",
    "body": "bake a cake",
    "state": "proposed",
    "proposed_by_id": 1,
    "proposed_to_account_id": 2
}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.resources.duet.errors}}
{% endhighlight %}
