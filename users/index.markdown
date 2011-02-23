---
layout: default
title: Users
---

## Users

### `/user`

creates a new duet user.

* **method**: `POST`
* **arguments**:
  * `first_name` <req>*</req>
  * `last_name` <req>*</req>
  * `email` <req>*</req>
  * `password` <req>*</req>
  * `password_confirmation` <req>*</req>
  * `phone` <req>*</req>
  * `gender` — 0: male, 1: female
  * `birthday` — YYYY-MM-DD 00:00:00 (no time included)
* **returns**: unique identifier for new user
* **authentication required**: no

<!-- /api/users/{user_id}/update

method: POST
arguments:
first_name
last_name
email
phone
gender — 0: male, 1: female
birthday — YYYY-MM-DD 00:00:00 (no time included)
returns: success/failure boolean
updates a user record.

/api/users/{user_id}/set_profile_image

method: POST
arguments:
photo* — file upload
returns: URL for new image
set a profile photo for an existing user.

/api/users/{user_id}/privacy

method: POST
arguments:
maximum — boolean (default: 0)
post_to_promenade — boolean (default: 1)
returns: n/a
change the global privacy for a user.

/api/users/{user_id}/reset_password

method: POST
arguments:
email*
returns: success/failure boolean
reset a user's password and send them an email with a new, generated password. they can change it later.

/api/users/{user_id}/change_password

method: POST
arguments:
old_password* — must match existing password
password*
password_confirmation* — must match new password
returns: success/failure boolean
change a user's password.

/api/users/{user_id}/circle

method: GET
arguments:
num_per_page — default: 10
page — default: 1
returns: array of users
paginated list users a single duet user is connected to.
 -->
