---
layout: default
resource: Account
resource_id: account-sign_in
title: Signing in an Account
---
Get the API key for an existing account based on a username/password combination.

### Request

<span class="method">POST</span> `{{site.api.base_url}}/{{site.api.version}}/account/sign_in`

#### Account Authentication Required

`false`

#### Parameters

<span class="required">*</span> - required

* `account[login]`<span class="required"> *</span> - can be either email or phone
* `account[password]`<span class="required"> *</span>

### Response

An account JSON object containing the `authentication_token` only

#### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.sign_in}}
{% endhighlight %}

#### `401 Unauthorized`

