---
layout: default
title: Authentication
---
# {{page.title}}

There are two levels of authentication: application-level and account-level.  Application-level authentication is required for all API requests.  Account-level authentication is required for many but not all API methods.  Whether or not account-level authentication is required is noted on each API method's page under the **Account Authentication Required** heading.

## Methods of Authentication

Authentication is attained by sending the authentication tokens via special request headers.

### Application-level Authentication

Set the `X-Application-Token` request header with the value of application token given to you by the Duet team.  Each application (iphone, ipad, android, etc.) that integrates with the Duet API will have its own application token.

### Account-level Authentication

Set the `X-Account-Token` request header with the value of the `authentication_token` for the account you are authenticating as.

#### Fetching the `authentication_token`

The `authentication_token` for an account can be obtained via the [`POST account/sign_in`](/post/account/sign_in) API method.  `login` and `password` parameters are sent to this method and a JSON object containing the matching account's `authentication_token` is returned.

## Response if Authentication Fails

If an API method requires authentication and authentication fails, a `401 Unauthorized` response is returned.