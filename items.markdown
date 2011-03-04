---
layout: default
title: Items
---

## Items

### `/duets/:duet_id/items`

creates a item in a duet.

* **method**: `POST`
* **arguments**:
  * `note`
  * `photo` - file upload
  * `video` - file upload
* **returns**: item object (including URLs for photo/video where necessary)

### `/duets/:duet_id/items/:item_id/destroy`

deletes an item in a duet.

* **method**: `POST`
