---
layout: default
resource: Authentication
resource_id: authentication-overview
title: Overview
---
There are two levels of authentication: application-level and account-level.  Application-level authentication is required for all API requests.  Account-level authentication is required for many but not all API methods.  Whether or not account-level authentication is required is noted on each API method's page under the **Account Authentication Required** heading.

### Methods of Authentication

Authentication is attained by sending the authentication tokens via special request headers.

#### Application-level Authentication

Set the `X-Application-Token` request header with the value of application token given to you by the Duet team.  Each application (iphone, ipad, android, etc.) and version that integrates with the Duet API will have its own application token.

#### Account-level Authentication

Set the `X-Account-Token` request header with the value of the `authentication_token` for the account you are authenticating as.

##### Fetching the `authentication_token`

The `authentication_token` for an account can be obtained via the [`POST account/sign_in`](/1/post/account/sign_in) API method.  `login` and `password` parameters are sent to this method and a JSON object containing the matching account's `authentication_token` is returned.

### Response if Authentication Fails

If an API method requires authentication and authentication fails, a `401 Unauthorized` response is returned.

### Other Headers

The following other informational headers should be sent along with each request:

* `X-Device-Identifier` - The unique identifier of the device sending the request.  e.g. on an iPhone, the `uuid`.
* `X-Device-Push-Token` – The token (in hexadecimal format) needed to send push notifications if it exists. This would not be sent if a user opts out of push for our app. This token, if sent, should be represented as an uppercase string, 64 characters long, without spaces or other separators. e.g.

    FE66489F304DC75B8D6E8200DFF8A456E8DAEACEC428B427E9518741C92C6660
* `X-Device-Software-Version` - The version of the operating system the device is running.
* `X-Location-Lat` - The current latitude of the device if GPS-enabled.
* `X-Location-Long` - The current longitude of the device if GPS-enabled.
* `X-Device-Language` – The preferred language string the user has set on their device. See this for more info on how to get that setting.
