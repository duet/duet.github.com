---
layout: default
resource: Account
resource_id: account-show
title: View account details
---
Get information for the currently authenticated account.

### Request

<span class="method">GET</span> `{{site.api.base_url}}/{{site.api.version}}/account`

#### Account Authentication Required

`true`

### Response

An account JSON object.

#### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}
