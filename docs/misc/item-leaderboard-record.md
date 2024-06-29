# `ItemLeaderboardRecord`

`ItemLeaderboardRecord` provides information of an item leaderboard record.

## Syntax

```ts
type ItemLeaderboardRecord = {
    name: string
    rank: Text | (string & {})
    player: string
    value: Text | (string & {})
}
```

## Examples

```json
{
    "name": "...",
    "rank": "...",
    "player": "...",
    "value": "..."
}
```
