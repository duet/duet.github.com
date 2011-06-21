---
layout: default
title: POST duets/:duet_id/propose
---
# `{{page.title}}`

Propose a duet to either an account in your circle or a phone number.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/propose`

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

### `200 OK`

A Duet object. See the [Duet Object documentation](/duet_object) for more information.

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.api.resources.duet.errors}}
{% endhighlight %}
