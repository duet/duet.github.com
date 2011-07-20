---
layout: default
resource: Account
resource_id: account-circle
title: View an account's circle
---
A paginated list of accounts the authenticated account is connected to.

### Request

<span class="method">GET</span> `{{site.api.base_url}}/{{site.api.version}}/account/circle`

#### Account Authentication Required

`true`

### Response

An array of account JSON objects.

#### `200 OK`

The `activity` node contains a count of un-viewed activity related to each account.

{% highlight javascript %}
{{site.api.resources.account.collection}}
{% endhighlight %}