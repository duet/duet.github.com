---
layout: default
title: GET account/privacy
---
# `{{page.title}}`

Get account privacy information.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/privacy`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`

## Response

A JSON object containing privacy settings for the account.

### `200 OK`

{% highlight javascript linenos %}
{{site.resources.account.privacy}}
{% endhighlight %}
