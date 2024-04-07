# `POST /sonolus/rooms/{name}`

`/sonolus/rooms/{name}` allows Sonolus app to join a room.

## Query Parameters

| Query Parameter   | Value | Description                                                                                |
| :---------------- | :---- | :----------------------------------------------------------------------------------------- |
| Create Parameters | `any` | Optional, see [Options Query Parameters](../query-parameters/options-query-parameters.md). |

## Request Headers

| Header              | Value    | Description                                                                              |
| :------------------ | :------- | :--------------------------------------------------------------------------------------- |
| `Sonolus-Signature` | `string` | See [`Sonolus-Signature`](../headers/sonolus-signature.md).                              |
| `Sonolus-Room-Key`  | `string` | Optional, see [`POST /sonolus/rooms/create`](../endpoints/post-sonolus-rooms-create.md). |

## Request Body

```ts
type JoinRoomRequest = {
    type: 'authenticateMultiplayer'
    address: string
    room: string
    time: number
    userProfile: UserProfile
}
```

### `type`

Server should verify that `type` equals to `'authenticateMultiplayer'`.

### `address`

Server should verify that `address` matches server address.

### `time`

Server should verify that `time` is recent.

## Response Code

| Code               | Description                         |
| :----------------- | :---------------------------------- |
| `200 OK`           |                                     |
| `401 Unauthorized` | Authentication required or expired. |

## Response Headers

| Header            | Value    | Description                                                       |
| :---------------- | :------- | :---------------------------------------------------------------- |
| `Sonolus-Version` | `string` | Optional, see [`Sonolus-Version`](../headers/sonolus-version.md). |

## Response Body

```ts
type JoinRoomResponse = {
    url: string
    type: 'round'
    session: string
}
```

### `url`

Url of multiplayer server.

### `type`

Type of multiplayer room.

Currently only `'round'` is supported.

### `session`

Server defined session information.

## Examples

```json
{
    "url": "wss://...",
    "type": "round",
    "session": "..."
}
```

## Remarks

Server should verify that request body is authentic using `Sonolus-Signature` request header.

If a room is being created, create query parameters and `Sonolus-Room-key` header will be available.

If successful, client will join the multiplayer server with `Sonolus-Room-Session` header containing the value of `session`. Server can use it to replay necessary information to multiplayer server.
