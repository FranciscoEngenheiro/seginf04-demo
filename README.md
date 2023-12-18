### Game Representation

> [!IMPORTANT]
> The `state` property can only be `in_progress` or `finished`.
> 
> The `winner` property can only be `B` or `W`.
> 
> The `turn` property can only be `B` or `W`.
> 
> Both `winner` and `turn` properties might not be present in the representation, depending on the game state.
> 
> The `createdAt` and `updatedAt` properties are in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format `YYYY-MM-DDTHH:MM:SSZ`.
> 
> Moves in the `grid` property are represented as `colrow-player` format where `col` is the column,
> `row` is the row and `player` is the player that made the move (w-White, b-Black).

```json
{
  "id": 87,
  "state": {
      "name": "finished"
  },
  "variant": {
      "id": 1,
      "name": "freestyle",
      "openingRule": "none",
      "boardSize": 15
  },
  "board": {
      "grid": [
          "a7-w"
      ],
      "winner": "B"
  },
  "createdAt": "2023-12-18T13:50:34Z",
  "updatedAt": "2023-12-18T14:00:56Z",
  "hostId": 895,
  "guestId": 896
}
```