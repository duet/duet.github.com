---
layout: default
resource: General
resource_id: general-information
title: General Information
---

### Format

All API responses will be in JSON format unless there is nothing to return.  If that is the case, only an HTTP status code will be returned.

<h3 id="pagination">Pagination on collection methods</h3>

All API methods that return collections of objects will have pagination applied to them.  The default settings can be adjusted by passing the following parameters with your request.

* `per` - default: 10
* `page` - default: 1

### Timestamps

All timestamps will be provided in [rfc2822 format](http://tools.ietf.org/html/rfc2822#section-3.3).  e.g. `Thu, 30 Jun 2011 02:23:58 -0400`