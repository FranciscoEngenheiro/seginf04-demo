### Game Representation

> [!IMPORTANT]
> The `state` property can only be `in_progress` or `finished`.
>
> The `winner` property can only be `B` or `W`.
>
> The `turn` property can only be `B` or `W`.
>
> Both `winner` and `turn` properties might not be present in the representation, depending on the game state:
> - If the state is `in_progress` the `turn` property is present.
> - If the state is `finished`, the `turn` property is not present.
> To determine between a draw or a win, the `winner` property presence must be checked.
>
> The `createdAt` and `updatedAt` properties are in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601)
> format `YYYY-MM-DDTHH:MM:SSZ`.
>
> Moves in the `grid` property are represented as `colrow-player` format where `col` is the column,
> `row` is the row and `player` is the player that made the move (`w`-White, `b`-Black).