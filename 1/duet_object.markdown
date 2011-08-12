---
layout: default
resource: Duets
resource_id: duets-overview
title: Overview
---
A Duet object returned in an API response will vary depending on the state it is in.  The Duet object will mostly vary when it is in an unpaired or proposed state.  Once it becomes active, its format becomes much more predictable.

This page aims to provide an overview of what you can expect when parsing an API response containing Duets.

### JSON Responses

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
            "first_name": "Ubaldo",
            "image": {
              "large": "http://cdn.duet.me/uploads/account/image/22/large_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "medium": "http://cdn.duet.me/uploads/account/image/22/medium_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "full": "http://cdn.duet.me/uploads/account/image/22/full_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "medium@2x": "http://cdn.duet.me/uploads/account/image/22/medium2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "full@2x": "http://cdn.duet.me/uploads/account/image/22/full2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "large@2x": "http://cdn.duet.me/uploads/account/image/22/large2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "state": "current"
            }
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
            "id": 2,
            "first_name": "Ubaldo",
            "image": {
              "large": "http://cdn.duet.me/uploads/account/image/22/large_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "medium": "http://cdn.duet.me/uploads/account/image/22/medium_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "full": "http://cdn.duet.me/uploads/account/image/22/full_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "medium@2x": "http://cdn.duet.me/uploads/account/image/22/medium2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "full@2x": "http://cdn.duet.me/uploads/account/image/22/full2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "large@2x": "http://cdn.duet.me/uploads/account/image/22/large2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "state": "current"
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
            "first_name": "Ubaldo",
            "image": {
              "large": "http://cdn.duet.me/uploads/account/image/22/large_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "medium": "http://cdn.duet.me/uploads/account/image/22/medium_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "full": "http://cdn.duet.me/uploads/account/image/22/full_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "medium@2x": "http://cdn.duet.me/uploads/account/image/22/medium2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "full@2x": "http://cdn.duet.me/uploads/account/image/22/full2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "large@2x": "http://cdn.duet.me/uploads/account/image/22/large2x_e2512060-948c-012e-1bfb-4040900bc90c.jpg",
              "state": "current"
            }
        },
        "body": "watch a movie",
        "prefix": "Let's",
        "id": 2,
        "state": "proposed",
        "activity": 1
    }
}
{% endhighlight %}

#### Video attachment

If a video was sent along with the duet when it was proposed, the duet object will also contain `video` and `image` nodes.  The structure is the same as a duet item's `video` and `image`.

{% highlight javascript %}
{
    "duet": {
        "proposed_to": {
            "phone": null,
            "image": {
                "medium": "http://cdn.duet.me/default/medium_propose_to_phone_number_image.png",
                "mini": "http://cdn.duet.me/default/mini_propose_to_phone_number_image.png",
                "small": "http://cdn.duet.me/default/small_propose_to_phone_number_image.png",
                "original": "http://cdn.duet.me/default/original_propose_to_phone_number_image.png"
            },
            "first_name": null
        },
        "proposed_by_me": true,
        "body": "ratione non architecto",
        "prefix": "Let's",
        "activity": 0,
        "proposed_to_account": false,
        "id": 2,
        "video": "http://cdn.duet.me/uploads/item/video/1/9143fba0-a69d-012e-efba-001b63bb2354.m4v",
        "image": {
            "url": "http://cdn.duet.me/uploads/item/image/1/9143d840-a69d-012e-efb9-001b63bb2354.png",
            "height": 100,
            "width": 100
        },
        "state": "unpaired"
    }
}
{% endhighlight %}

#### Activity

The `activity` node contains a count of un-viewed activity related to the duet.

<h4 id="declined-and-canceled">Declined &amp; Canceled Duets</h4>

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


<h3 id="object-lifecycle">Object Lifecycle</h3>

A duet object goes through several different states during its lifespan and there are specific actions that can be called on a duet to move it from one state to another.  The diagram below illustrates this (click to view full diagram).

<a href="/images/duet-object-lifecycle.png"><img src="/images/duet-object-lifecycle-thumb.png" alt="{{page.title}}"></a>

Some important notes:

<ul class="text">
  <li>Once a duet has been proposed to someone, it can only be accepted or declined by that person. It can, however, be canceled by the person who proposed it.</li>
  <li>If a duet is declined by the person you proposed it to, the person who proposed the duet will be given the opportunity to view why and then the duet will be removed from their stream.</li>
  <li>Once a proposed duet is accepted it will be in the active state.  From there is can be canceled or completed by either of the parties involved in the duet.</li>
  <li>If a duet is active and is canceled by one of the participating parties, it is moved into the canceled state.  The other party involved will have an opportunity to see why the duet has been canceled, then the duet will be removed from their stream.</li>
</div>