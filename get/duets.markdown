---
layout: default
title: GET duets
---
# `{{page.title}}`

A paginated list of all duets related to the currently authenticated account.  This includes both duets proposed by the current account and duets proposed to the current account.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets`

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

An array of duet JSON objects.

### HTTP Code

`200 OK`

### JSON

{% highlight javascript linenos %}
{{site.resources.duet.collection}}
{% endhighlight %}