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

Which is AES-CBC-256 encrypted with key and IV associated with the session, and then base64 encoded.

## Examples

```http
Sonolus-Session-Data: ...
```

## Remarks

[`Sonolus-Session-Id`](./sonolus-session-id.md) must also present.

Using session id specified by [`Sonolus-Session-Id`](./sonolus-session-id.md), server can look up information (key, IV, and expiration) associated with the session. Server must first verify that the session has not expired, then use key and IV to decrypt session data.

Once decrypted, server must first verify that `address` is allowed, then allow or reject the request depending on `userProfile`.
