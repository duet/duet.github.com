---
layout: default
title: Accounts
---
### `/account/update_privacy`

change the global privacy for an account.

* **method**: `POST`
* **arguments**:
  * `maximum` - boolean (default: 0)
  * `post_to_promenade` - boolean (default: 1)
* **returns**: `200 OK`

### `/account/reset_password`

reset an account's password and send them an email with a new, generated password. they can change it later.

* **method**: `POST`
* **arguments**:
  * email <req>*</req>
* **returns**: `200 OK` or `422 Unprocessable Entity`

### `/account/change_password`

change an account's password.

* **method**: `POST`
* **arguments**:
  * `old_password` <req>*</req> - must match existing password
  * `password` <req>*</req>
  * `password_confirmation` <req>*</req> - must match new password
* **returns**: `200 OK` or `422 Unprocessable Entity`

### `/account/circle`

paginated list accounts a single duet account is connected to.

* **method**: `GET`
* **arguments**:
  * `per` - default: 10
  * `page` - default: 1
* **returns**: array of accounts
