# `POST /sonolus/authenticate`

`/sonolus/authenticate` allows Sonolus app to establish an authentication session.

## Query Parameters

None.

## Request Headers

None.

## Request Body

None.

## Response Code

| Code            | Description                                   |
| :-------------- | :-------------------------------------------- |
| `200 OK`        |                                               |
| `404 Not Found` | Authentication not supported or not required. |

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type AuthenticateInfo = {
    address: string
    session: string
    expiration: number
}
```

### `address`

Sonolus app will verify if `address` matches server address in app for security.

### `session`

Session information, contains:

```ts
type SessionInfo = {
    id: string
    key: string
    iv: string
}
```

Which is RSA-OAEP-SHA1 encrypted with Sonolus encryption public key:

```
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA8DDWNplPkFiQI2QywLOT
OLAsIA+H0kc9RjFK4pJV6MKJxvhAGsJ8uA18Wsug4YU7Kp93gV3Zv7/RlV0yMkWv
CxhsQO/K9NI5MdyJSxTI7UcVukZDAQbiFBT+/1od28XKhn6eO2PqI3E7uXpN44Cd
O7rgtLSYBBT1/+Aw/gJHn+u5fo60xusfPEYYpXNnIHEL52niNW52wmk/LGItZDlJ
+oSwZH2qRFol6t63ymzFUNbred0DwJD+RmqWEq/J/57ofCaL65148BmD2KkJoA8k
MR4hNOP9cYs7iQQguboCa0SsJPl4V2SOG+Mn6IkSkZJRfYkC3SXdjmxf+i4qA801
RQIDAQAB
-----END PUBLIC KEY-----
```

And then base64 encoded.

Session information should be created freshly with each authentication request, cryptographically random, and stored for session verification later.

#### `id`

Session id.

#### `key`

An AES-CBC-256 encryption key associated with this session.

#### `iv`

An AES-CBC-256 encryption IV associated with this session.

### `expiration`

Session expiration time, in Unix timestamp in milliseconds.

Session should be short lived, recommended 30 minutes or less. Once expired, Sonolus app will initiate re-authentication process automatically.

## Examples

```json
{
    "address": "https://...",
    "session": "...",
    "expiration": 1640995200000
}
```
