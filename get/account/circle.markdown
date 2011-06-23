---
layout: default
title: GET account/circle
---
# `{{page.title}}`

A paginated list of accounts the authenticated account is connected to.

## URL

`{{site.api.base_url}}/{{site.api.version}}/account/circle`

## Format

JSON

## HTTP Method

`GET`

## Account Authentication Required

`true`
## Parameters

### Optional

* `per` - default: 10
* `page` - default: 1

## Response

An array of account JSON objects.

### HTTP Code

`200 OK`

### JSON

The `activity` node contains a count of un-viewed activity related to each account.

{% highlight javascript linenos %}
{{site.api.resources.account.collection}}
{% endhighlight %}