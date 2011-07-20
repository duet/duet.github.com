---
layout: default
resource: Account
resource_id: account-update
title: Update an account
---
Update basic account information.  This does not include password or image updating.

### Request

<span class="method">POST</span> `{{site.api.base_url}}/{{site.api.version}}/account/update`

#### Account Authentication Required

`true`

#### Parameters

<span class="required">*</span> - required

* `account[first_name]`
* `account[last_name]`
* `account[email]`
* `account[phone]`

### Response

An account JSON object.  **Note**: You cannot update an account's [password](/1/post/account/change_password) or [profile image](/1/post/account/image) from this method.  Use the respective methods available to handle those needs.

#### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}

#### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.account.errors}}
{% endhighlight %}
