---
layout: default
resource: Duets
resource_id: duets-acknowledge-decline
title: Acknowledge a duet has been declined
---
Once the decline has been acknowledged, it will no longer appear in your account. This will only work if you were not the party who declined the duet.

### Request

<span class="method">POST</span> `{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id/acknowledge_decline`

#### Account Authentication Required

`true`

### Response

#### `200 OK`

#### `422 Unprocessable Entity`

#### `404 Not Found`
