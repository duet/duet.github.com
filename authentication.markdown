---
layout: default
title: Authentication
---
# {{page.title}}

Authentication is required for many of the API methods available.  Whether or not it is required is noted on each API method's page under the **Authentication Required** heading.

## Methods of Authentication

Authentication is attained by sending the `authentication_token` for a given account along with each request it's required for.  There are two methods of doing this:

1. Setting the `X-Token` request header with the value of `authentication_token`.
2. Sending an HTTP parameter called `token` with the value set to `authentication_token`.

Of these two methods, the `X-Token` header option is preferred just because it's cleaner and keeps all HTTP parameters sent related to the individual API method and not Authentication.

## Fetching the `authentication_token`

The `authentication_token` for an account can be obtained via the [`POST account/sign_in`](/post/account/sign_in) API method.  `email` and `password` parameters are sent to this method and a JSON object containing the matching account's `authentication_token` is returned.