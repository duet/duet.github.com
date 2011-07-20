---
layout: default
resource: Duets
resource_id: duets-show
title: Get a specific duet
---
Get duet matching the specified `:duet_id`.

### Request

<span class="method">GET</span> `{{site.api.base_url}}/{{site.api.version}}/duets/:duet_id`

#### Account Authentication Required

`true`

### Response

#### `200 OK`

A Duet object. See the [Duet Object documentation](/1/duet_object) for more information.
