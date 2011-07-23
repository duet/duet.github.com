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

An account JSON object. **Note**: `account[image][state]` will always be 1 of 2 values: `current` or `processing`.  If the image state is `processing`, in the profile view of the application, the "New Profile Photo" button should be disabled and the icon showing your account image be replaced with some sort of loading indicator.  The client should then poll the [account details](/1/get/account) API method until `account[image][state]` returns to `current`.  At that point, the "New Profile Photo" button can be re-enabled and the new photo (returned by the API response) can be displayed in their profile view.

All other views in the application can disregard the `account[image][state]` property and continue to use the values of the various image sizes normally.

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
