# `Sonolus-Session-Id`

`Sonolus-Session-Id` specifies the current session id.

## Syntax

```http
Sonolus-Session-Id: <value>
```

## Examples

```http
Sonolus-Session-Id: ...
```

## Remarks

[`Sonolus-Session-Data`](./sonolus-session-data) must also present.

Session id is the same as returned by [`POST /sonolus/authenticate`](../endpoints/post-sonolus-authenticate).

Using session id, server can look up information (key, IV, and expiration) associated with the session. Server must first verify that the session has not expired, then use key and IV to decrypt [`Sonolus-Session-Data`](./sonolus-session-data).
