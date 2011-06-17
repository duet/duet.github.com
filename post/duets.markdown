---
layout: default
title: POST duets
---
# `{{page.title}}`

Creates a new duet with the current account as the proposer.

## URL

`{{site.api.base_url}}/{{site.api.version}}/duets`

## Format

JSON

## HTTP Method

`POST`

## Account Authentication Required

`true`

## Parameters

### Required

* `duet[body]` - limit 100 characters

### Optional

* `duet[video]` - a video in m4v format
* `duet[propose_to][account_id]` - `id` of an account in your circle you want to propose this duet to
* `duet[propose_to][phone]` - The phone number of a person you'd like to duet with.  An attempt will be made to find an existing account with the same phone number.  If one is found, that person will be notified via push notification about the duet.  If no matching account is found, an SMS message will be sent to that phone number with an invite.
* `duet[propose_to][first_name]` - The first name of the person you're proposing this duet to.  Only necessary if you're proposing to a phone number.
* `duet[propose_to][last_name]` - `The last name of the person you're proposing this duet to.  Only necessary if you're proposing to a phone number.

## Response

A duet object.

### `200 OK`

If `duet[propose_to]` isn't set, the response will be a basic Duet object:

{% highlight javascript linenos %}
{
    "duet": {
        "proposed_by_me": true,
        "body": "watch a movie",
        "prefix": "Let's",
        "id": 2,
        "state": "unpaired"
    }
}
{% endhighlight %}

If the duet is being proposed to an account in their circle or an account match via phone number happened, `proposed_by_me` and `proposed_by_account` will be `true`:

{% highlight javascript linenos %}
{
    "duet": {
        "proposed_by_me": true,
        "proposed_to_account": true,
        "proposed_to": {
            "id": 2,
            "gender": null,
            "phone": "747724958744",
            "last_name": "Eichmann",
            "image": {
                "medium": "http://cdn.duet.me/default/medium_account_image.png",
                "mini": "http://cdn.duet.me/default/mini_account_image.png",
                "small": "http://cdn.duet.me/default/small_account_image.png",
                "original": "http://cdn.duet.me/default/original_account_image.png"
            },
            "first_name": "Ubaldo",
            "email": "account-44@email.com",
            "born_on": null
        },
        "body": "watch a movie",
        "prefix": "Let's",
        "id": 2,
        "state": "proposed"
    }
}
{% endhighlight %}

If the duet is being proposed to a phone number (no matching accounts could be found), `proposed_to` will only contain `phone` and `first_name` and `last_name` if they were provided, and `proposed_to_account` will be `false`.

{% highlight javascript linenos %}
{
    "duet": {
        "proposed_to": {
          "phone": "747724958744",
          "last_name": "Eichmann",
          "first_name": "Ubaldo"
        },
        "proposed_by_me": true,
        "body": "aut dolor id",
        "prefix": "Let's",
        "proposed_to_account": false,
        "id": 2,
        "video": "http://cdn.duet.me/uploads/duet/video/2/video.m4v",
        "state": "proposed"
    }
}
{% endhighlight %}

If the duet was proposed to me by someone else `proposed_by_me` will be false and the `proposed_by` node will have the proposer's account information.

{% highlight javascript linenos %}
{
    "duet": {
        "proposed_by_me": false,
        "proposed_by": {
            "id": 2,
            "gender": null,
            "phone": "747724958744",
            "last_name": "Eichmann",
            "image": {
                "medium": "http://cdn.duet.me/default/medium_account_image.png",
                "mini": "http://cdn.duet.me/default/mini_account_image.png",
                "small": "http://cdn.duet.me/default/small_account_image.png",
                "original": "http://cdn.duet.me/default/original_account_image.png"
            },
            "first_name": "Ubaldo",
            "email": "account-44@email.com",
            "born_on": null
        },
        "body": "watch a movie",
        "prefix": "Let's",
        "id": 2,
        "state": "proposed"
    }
}
{% endhighlight %}

### `422 Unprocessable Entity`

{% highlight javascript linenos %}
{{site.api.resources.duet.errors}}
{% endhighlight %}
