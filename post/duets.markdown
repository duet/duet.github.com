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
* `duet[propose_to][account_id]` - `id` of an account in your circle you want to propose this duet to
* `duet[propose_to][phone]` - The phone number of a person you'd like to duet with.  An attempt will be made to find an existing account with the same phone number.  If one is found, that person will be notified via push notification about the duet.  If no matching account is found, an SMS message will be sent to that phone number with an invite.
* `duet[propose_to][first_name]` - The first name of the person you're proposing this duet to.  Only necessary if you're proposing to a phone number.
* `duet[propose_to][last_name]` - The last name of the person you're proposing this duet to.  Only necessary if you're proposing to a phone number.
* `duet[propose_to][image]` - An image of the person you're proposing this duet to.  Only necessary if you're proposing to a phone number and an image in the mobile device's address book is available.

## Response

### `200 OK`

A Duet object. See the [Duet Object documentation](/duet_object) for more information.

### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.duet.errors}}
{% endhighlight %}
