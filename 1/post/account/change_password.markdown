---
layout: default
resource: Account
resource_id: account-change_password
title: Change password
---
Change the password for the currently authenticated account.

### Request

<span class="method">POST</span> `{{site.api.base_url}}/{{site.api.version}}/account/change_password`

#### Account Authentication Required

`true`

#### Parameters
<span class="required">*</span> - required

* `account[password]`<span class="required"> *</span>
* `account[password_confirmation]`<span class="required"> *</span>

### Response

A account JSON object.

#### `200 OK`

{% highlight javascript %}
{{site.api.resources.account.basic}}
{% endhighlight %}

#### `422 Unprocessable Entity`

{% highlight javascript %}
{
    "errors" : {
        "password": [
          "doesn't match confirmation"
        ]
    }
}
{% endhighlight %}
