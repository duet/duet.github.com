---
layout: default
resource: Duets
resource_id: duets-acknowledge-cancel
title: Acknowledge a duet has been canceled
---
Once the cancel has been acknowledged, it will no longer appear in your account. This will only work if you were not the party who canceled the duet.

### Request

<span class="method">POST</span> `{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/acknowledge_cancel`

#### Account Authentication Required

`true`

### Response

#### `200 OK`

#### `422 Unprocessable Entity`

#### `404 Not Found`
