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

A duet object.

### `200 OK`

If the duet is being proposed to a phone number it will look like so:

{% highlight javascript linenos %}
{{site.api.resources.duet.proposed_to_phone_number}}
{% endhighlight %}

If the duet is being proposed to an account in their circle it will look like so:

{% highlight javascript linenos %}
{{site.api.resources.duet.proposed_to_account}}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.api.resources.duet.errors}}
{% endhighlight %}
