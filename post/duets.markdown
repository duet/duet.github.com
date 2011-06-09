---
layout: default
title: POST duets
---
# `{{page.title}}`

Creates a new duet with the current account as the proposer.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `duet[body]` - limit 100 characters

### Optional

* `duet[video]` - a video in m4v format
* `duet[propose_to]` - `id` of account in your circle or phone number of person that isn't in your circle you want to propose this duet to.

## Response

A duet object.

### `200 OK`

If `duet[propose_to]` isn't set, the response will be a basic Duet object:

{% highlight javascript linenos %}
{{site.api.resources.duet.basic}}
{% endhighlight %}

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
