---
layout: default
title: Duets
---

## Duets

### `/duets/public`

Returns a list of publicly available duets for use in public areas of the app in reverse-chronological order.

* **method**: `GET`
* **arguments**:
  * `per` - default: 10
  * `page` - default: 1
* **returns**: array of duets sorted by date DESC
* **authentication required**: no

### `/duets/public/featured`

Returns a list of featured duets for use in public areas of the app.

* **method**: `GET`
* **arguments**:
  * `per` - default: 10
  * `page` - default: 1
* **returns**: array of duets
* **authentication required**: no


### `/duets`

Returns a list of all duets related to the current account.

* **method**: `GET`
* **arguments**:
  * `per` - default: 10
  * `page` - default: 1
* **returns**: array of duets sorted by date DESC

### `/duets/proposed`

Returns a list of all proposed duets related to the current account.

* **method**: `GET`
* **arguments**:
  * `per` - default: 10
  * `page` - default: 1
* **returns**: array of duets sorted by date DESC

### `/duets/completed`

Returns a list of all completed duets related to the current account.

* **method**: `GET`
* **arguments**:
  * `per` - default: 10
  * `page` - default: 1
* **returns**: array of duets sorted by date DESC


### `/duets/with/:second_user_id`

returns a list of the current user's duets that involve `:second_user_id`.

* **method**: `GET`
* **returns**: array of duets sorted by date DESC

### `/duets/:duet_id`

view a single duet.

* **method**: `GET`
* **returns**: duet object

### `/duets`

creates a new duet associated with the current user.

* **method**: POST
* **arguments**:
  * `title` <req>*</req>
  * `is_shared` - boolean (default: 0)
  * `is_ditto` - boolean (default: 0)
  * `privacy` - 0: private, 1: users included, 2: my circle, 4: public
* **returns**: duet object (including id)

### `/duets/:duet_id/update`

update an existing duet.

* **method**: `POST`
* **arguments**:
  * `title` <req>*</req>
  * `is_shared` - boolean (default: 0)
  * `is_ditto` - boolean (default: 0)
  * `privacy` - 0: private, 1: users included, 2: my circle, 4: public
* **returns**: duet object (including id)

### `/duets/:duet_id/complete`

mark a duet completed.

* **method**: `GET`

### `/duets/:duet_id/destroy`

destroy an existing duet and **all of its related items**.

* **method**: `GET`
