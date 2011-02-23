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
  * `gender` - 0: male, 1: female
  * `birthday` - `YYYY-MM-DD 00:00:00` (no time included)
* **returns**: unique identifier for new user
* **authentication required**: no

### `/user/update`

updates a user record.

* **method**: `POST`
* **arguments**:
  * `first_name` <req>*</req>
  * `last_name` <req>*</req>
  * `email` <req>*</req>
  * `password` <req>*</req>
  * `password_confirmation` <req>*</req>
  * `phone` <req>*</req>
  * `gender` - 0: male, 1: female
  * `birthday` - `YYYY-MM-DD 00:00:00` (no time included)
* **returns**: `200 OK` or `422 Unprocessable Entity`

### `/user/set_profile_image`

set a profile photo for an existing user.

* **method**: `POST`
* **arguments**:
  * `photo` <req>*</req> - file upload
* **returns**: URL for new image

### `/user/update_privacy`

change the global privacy for a user.

* **method**: `POST`
* **arguments**:
  * `maximum` - boolean (default: 0)
  * `post_to_promenade` - boolean (default: 1)
* **returns**: `200 OK`

### `/user/reset_password`

reset a user's password and send them an email with a new, generated password. they can change it later.

* **method**: `POST`
* **arguments**:
  * email <req>*</req>
* **returns**: `200 OK` or `422 Unprocessable Entity`

### `/user/change_password`

change a user's password.

* **method**: `POST`
* **arguments**:
  * `old_password` <req>*</req> - must match existing password
  * `password` <req>*</req>
  * `password_confirmation` <req>*</req> - must match new password
* **returns**: `200 OK` or `422 Unprocessable Entity`

### `/user/circle`

paginated list users a single duet user is connected to.

* **method**: `GET`
* **arguments**:
  * `num` - default: 10
  * `page` - default: 1
* **returns**: array of users
