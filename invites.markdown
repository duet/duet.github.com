---
layout: default
title: Invites
---

## Invites

### `/invites`

list of pending invites for a user.

* **method**: `GET`
* **returns**: array of invite objects

### `/invites/:invite_id/process`

accept or ignore an invite from a duet user.

* **method**: `POST`
* **arguments**:
  * `accept` <req>*</req> - boolean
