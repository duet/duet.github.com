---
layout: default
resource: Account
resource_id: account-image
title: Update account image
---
Set the profile photo for the currently authenticated account.

### Request

<span class="method">POST</span> `{{site.api.base_url}}/{{site.api.version}}/account/image`

#### Account Authentication Required

`true`

#### Parameters

<span class="required">*</span> - required

* `account[image]` - file upload in png, jpg, or gif format

### Response

An account JSON object.

#### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}

#### `422 Unprocessable Entity`

{% highlight javascript %}
{
    "errors" : {
        "image": ["is not an allowed file type"]
    }
}
{% endhighlight %}
