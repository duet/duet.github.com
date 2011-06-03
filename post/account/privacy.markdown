---
layout: default
title: POST account/privacy
---
# `{{page.title}}`

Update account privacy information. If `maximum_privacy` is set to true, `promenade_sharing` will be set to false regardless of what it sent.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/privacy`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

* `account[maximum_privacy]` - `1` or `0`
* `account[promenade_sharing]` - `1` or `0`

## Response

A JSON object containing privacy settings for the account.

### `200 OK`

{% highlight javascript linenos %}
{{site.api.resources.account.privacy}}
{% endhighlight %}

### `422 Unprocessable Entity`
