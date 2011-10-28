---
layout: default
resource: History
resource_id: history
title: Account history
---
Returns all data associated with the currently authenticated account. This method's main purpose is for seeding the local database after a fresh installation of the client application. In the case of accounts that are very active or very old, the response from the server could be quite large.

The data in this feed is cached once every 24 hours on the server, so after retrieving this data, it's recommended to fetch the account's [recent activity](/1/get/recent_activity) from the last 24 hours to make sure everything is current.

### Request

<span class="method">GET</span> `{{site.api.base_url}}/{{site.api.version}}/account/history`

#### Account Authentication Required

`true`

### Response

The format of this response is exactly the same as [recent activity](/1/get/recent_activity). A JSON object containing up to three collections `items`, `duets`, `circle`. If a collection has no data, it will not be present in the feed.

If an account has no history, no data will be returned, just a `200 OK` status.

#### `200 OK`

{% highlight javascript %}
{
    "items": [
        {
            "item": {
                "content_type": "message",
                "id": 12571,
                "duet_id": 2981,
                "message": "That sounds like a great idea!",
                "created_by_id": 11,
                "created_at": "Mon, 19 Sep 2011 14:46:50 -0400"
            }
        },
        {
            "item": {
                "content_type": "image",
                "id": 12561,
                "duet_id": 2981,
                "image": {
                    "url": "https://duet-assets-development.s3.amazonaws.com/uploads/item/image/12561/image.jpg",
                    "width": 961,
                    "height": 961
                },
                "created_by_id": 231,
                "created_at": "Mon, 19 Sep 2011 14:39:07 -0400"
            }
        },
        {
            "item": {
                "content_type": "message",
                "id": 12551,
                "duet_id": 2971,
                "message": "Oh sweet! ",
                "created_by_id": 51,
                "created_at": "Mon, 19 Sep 2011 12:20:30 -0400"
            }
        }
    ],
    "circle": [
        {
            "account": {
                "activity": 0,
                "id": 581,
                "last_activity_at": "Tue, 19 Jul 2011 21:05:40 -0400",
                "image": {
                    "medium": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/9f682df245668969bbcd5395bdc2882591eeecde/medium_image.jpg",
                    "medium@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/9f682df245668969bbcd5395bdc2882591eeecde/medium2x_image.jpg",
                    "large": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/9f682df245668969bbcd5395bdc2882591eeecde/large_image.jpg",
                    "full@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/9f682df245668969bbcd5395bdc2882591eeecde/full2x_image.jpg",
                    "large@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/9f682df245668969bbcd5395bdc2882591eeecde/large2x_image.jpg",
                    "full": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/9f682df245668969bbcd5395bdc2882591eeecde/full_image.jpg",
                    "state": "current"
                },
                "first_name": "Max"
            }
        }
    ],
    "duets": [
        {
            "duet": {
                "prefix": "Let’s",
                "proposed_by_me": false,
                "id": 2981,
                "proposed_by": {
                    "id": 231,
                    "image": {
                        "medium": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/medium_image.jpg",
                        "medium@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/medium2x_image.jpg",
                        "large": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/large_image.jpg",
                        "full@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/full2x_image.jpg",
                        "large@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/large2x_image.jpg",
                        "full": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/full_image.jpg",
                        "state": "current"
                    },
                    "first_name": "Jane"
                },
                "activity": 0,
                "updated_at": "Tue, 19 Jul 2011 21:05:40 -0400",
                "body": "fastforward to Friday",
                "state": "active"
            }
        },
        {
            "duet": {
                "prefix": "Let’s",
                "proposed_by_me": false,
                "id": 2971,
                "proposed_by": {
                    "id": 51,
                    "image": {
                        "medium": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/medium_image.jpg",
                        "medium@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/medium2x_image.jpg",
                        "large": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/large_image.jpg",
                        "full@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/full2x_image.jpg",
                        "large@2x": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/large2x_image.jpg",
                        "full": "https://duet-assets-development.s3.amazonaws.com/uploads/account/processed_image/eadc1dd8fc279583d5552700ae5d248e3fa123bd/full_image.jpg",
                        "state": "current"
                    },
                    "first_name": "Benjamin"
                },
                "activity": 0,
                "updated_at": "Tue, 19 Jul 2011 21:05:40 -0400",
                "image": {
                    "url": "https://duet-assets-development.s3.amazonaws.com/uploads/item/image/12511/image.jpg",
                    "width": 360,
                    "height": 480
                },
                "body": "go see a movie.",
                "state": "active"
            }
        }
    ]
}
{% endhighlight %}
