---
layout: default
resource: Account
resource_id: account-create
title: Create an account
---
Creates a new Duet account.

### Request

<span class="method">POST</span> `{{site.api.base_url}}/{{site.api.version}}/account`

#### Account Authentication Required

`false`

#### Parameters

<span class="required">*</span> - required

* `account[first_name]`<span class="required">*</span>
* `account[email]`<span class="required">*</span>
* `account[password]`<span class="required">*</span>
* `account[phone]`<span class="required">*</span>
* `account[image]`<span class="required">*</span> - file upload in png, jpg, or gif format

### Response

An account JSON object.  **Note**: If you want to sign the account in immediately after successfully creating it, an immediate call to [`POST account/sign_in`](/post/account/sign_in) should be made so the `authentication_token` can be retrieved.

Keep in mind that the image takes a short time to process on the server and will not be immediately available.  How this works is explained [here](/1/post/account/image).

#### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}

#### `422 Unprocessable Entity`

{% highlight javascript %}
{{site.api.resources.account.errors}}
{% endhighlight %}
