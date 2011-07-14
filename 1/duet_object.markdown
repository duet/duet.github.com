---
layout: default
title: Duet Object
---
# `{{page.title}}`

A Duet object returned in an API response will vary depending on the state it is in.  The Duet object will mostly vary when it is in an unpaired or proposed state.  Once it becomes active, its format becomes much more predictable.

This page aims to provide an overview of what you can expect when parsing an API response containing Duets.

## JSON Responses

When you create a duet, if `duet[propose_to]` isn't set, the response will be the simplest form of a Duet object:

{% highlight javascript %}
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

If the duet is being proposed to an account in your circle or an account match via phone number occurs, `proposed_by_me` and `proposed_by_account` will be `true`:

{% highlight javascript %}
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

If the duet is being proposed to a phone number and no matching accounts could be found, `proposed_to` will only contain `phone` as well as `first_name`, `last_name`, and `image` if they were provided. `proposed_to_account` will be `false`.

{% highlight javascript %}
{
    "duet": {
        "proposed_to": {
          "phone": "747724958744",
          "last_name": "Eichmann",
          "first_name": "Ubaldo",
          "image": {
              "medium": "/uploads/duet/propose_to_phone_number_image/2/medium_image.png",
              "mini": "/uploads/duet/propose_to_phone_number_image/2/mini_image.png",
              "small": "/uploads/duet/propose_to_phone_number_image/2/small_image.png",
              "original": "/uploads/duet/propose_to_phone_number_image/2/original_image.png"
          }
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

If the duet was proposed to you by someone else, `proposed_by_me` will be false and the `proposed_by` node will have the proposing account's information.

{% highlight javascript %}
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
        "state": "proposed",
        "activity": 1
    }
}
{% endhighlight %}

### Activity

The `activity` node contains a count of un-viewed activity related to the duet.

### Declined & Canceled Duets

If a duet is [declined](/1/post/duets/:duet_id/declined/) or [canceled](/1/post/duets/:duet_id/canceled/),  nodes telling you who, why, and when will be included in the duet object.  The `*_by` nodes will contain the account_id of the account that declined/canceled the duet.  The `*_why` will either be `null` or a string containing a message why the duet was declined or canceled.  The `*_at` will tell you when the action occurred.

{% highlight javascript %}
{
    "duet": {
        ...
        "declined_why": "I don't want to do that with you.",
        "declined_at": "Thu, 30 Jun 2011 02:23:58 -0400",
        "declined_by": 1,
        "state": "declined"
    }
}
{% endhighlight %}

{% highlight javascript %}
{
    "duet": {
        ...
        "canceled_why": "I don't want to do that with you.",
        "canceled_at": "Thu, 30 Jun 2011 02:23:58 -0400",
        "canceled_by": 1,
        "state": "canceled"
    }
}
{% endhighlight %}


<h2 id="object-lifecycle">Object Lifecycle</h2>

A duet object goes through several different states during its lifespan and there are specific actions that can be called on a duet to move it from one state to another.  The diagram below illustrates this.

<img src="/images/duet-object-lifecycle.png" alt="{{page.title}}">

Some important notes:

<ul class="text">
  <li>The body of duet can only be edited as long as a duet has not been proposed to someone (i.e. it is in the unpaired state).</li>
  <li>Once a duet has been proposed to someone, it can only be accepted or declined by that person.</li>
  <li>If a duet is declined by the person you proposed it to, the person who proposed the duet will be notified and then the duet will be destroyed.</li>
  <li>Once a proposed duet is accepted it will be in the active state.  From there is can be canceled or completed by either of the parties involved in the duet.</li>
  <li>If a duet is active and is canceled by one of the participating parties, it is moved into the canceled state.  The other party involved will then see a notification the duet has been canceled, then the duet will be destroyed.</li>
</div>