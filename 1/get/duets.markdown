---
layout: default
resource: Duets
resource_id: duets-list
title: List my duets
---
A paginated list of all duets related to the currently authenticated account.  This includes both duets proposed by the current account and duets proposed to the current account.

### Request

<span class="method">GET</span> `{{site.api.base_url}}/{{site.api.version}}/duets`

#### Account Authentication Required

`true`

#### Parameters

<span class="required">*</span> - required

* `filter` - filter duets by their current state. valid options are `proposed`, `active`, and `completed`.
* `per` and `page` - see [pagination parameters](/1/general#pagination)

### Response

An array of Duet objects.

#### `200 OK`

See the [Duet Object documentation](/1/duet_object) for more information.
