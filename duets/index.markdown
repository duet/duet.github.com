---
layout: default
title: Duets
---

## Duets

### `/duets/public`

Returns a list of publicly available duets for use in public areas of the app in reverse-chronological order.

* **method**: `GET`
* **arguments**:
  * `num` — default: 10
* **returns**: array of duets sorted by date DESC
* **authentication required**: no

### `/duets/featured`

Returns a list of featured duets for use in public areas of the app.

* **method**: `GET`
* **arguments**:
  * `num` — default: 10
* **returns**: array of duets
* **authentication required**: no


