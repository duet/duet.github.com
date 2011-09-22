---
layout: default
resource: Recent Activity
resource_id: recent-activity
title: List recent activity
---
All recently updated duets, items and circle members having to do with you.

**Note:** The further back you go with the `since` parameter, the longer this method will take to respond. Keep this in mind in regards to your timeout threshold and only go as far as back as you absolutely need to.

### Request

<span class="method">GET</span> `{{site.api.base_url}}/{{site.api.version}}/recent_activity`

#### Account Authentication Required

`true`

#### Parameters

<span class="required">*</span> - required

* `since` - timestamp in integer format to tell the server how far back you want to go. **Defaults to 1 hour ago**.

### Response

A JSON object containing up to three collections `items`, `duets`, `circle`. If a collection has no data, it will not be present in the feed.

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
