---
layout: default
resource: Duets
resource_id: duets-with-person
title: List all duets with a particular person
---
A paginated list of all duets between the account specified by `:with_id` and the currently authenticated account.

### Request

<span class="method">GET</span> `{{site.api.base_url}}/{{site.api.version}}/duets/with/:with_id`

#### Account Authentication Required

`true`

#### Parameters

<span class="required">*</span> - required

* `per` and `page` - see [pagination parameters](/1/general#pagination)

### Response

An array of Duet objects.

#### `200 OK`

See the [Duet Object documentation](/1/duet_object) for more information.
