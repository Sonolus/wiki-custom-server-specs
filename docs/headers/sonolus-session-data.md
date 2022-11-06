# `Sonolus-Session-Data`

`Sonolus-Session-Data` specifies the current session data.

## Syntax

```http
Sonolus-Session-Data: <value>
```

Value contains:

```ts
type SessionData = {
    address: string
    userProfile: UserProfile
}
```

Which is AES-CBC-256 encrypted with key and IV associated with session id specified in [`Sonolus-Session-Id`](./sonolus-session-id.md), and then base64 encoded.

## Examples

```http
Sonolus-Session-Data: ...
```

## Remarks

[`Sonolus-Session-Id`](./sonolus-session-id.md) must also present.

Session id is the same as returned by [`POST /sonolus/authenticate`](../endpoints/post-sonolus-authenticate.md).

Using session id, server can look up information (key, IV, and expiration) associated with the session. Server must first verify that the session has not expired, then use key and IV to decrypt [`Sonolus-Session-Data`](./sonolus-session-data.md).

Once decrypted, server must first verify that `address` is allowed, then allow or reject the request depending on `userProfile`.
