## Features

- Allows Sam Sites to target CH47 Helicopters (Chinooks)
- Allows Sam Sites to target Patrol Helicopters

If you are looking to prevent Sam Sites from targeting your own Minicopters, Scrap Transport Helicopters, etc., then look for that feature in other plugins such as [SAM Site Authorization](https://umod.org/plugins/sam-site-authorization).

## Permissions

- `helisams.ch47.npc` -- Allows the player's Sam Sites to target the **NPC** CH47 Helicopters.
- `helisams.ch47.player` -- Allows the player's Sam Sites to target **player** CH47 Helicopters.
- `helisams.patrolheli` -- Allows the player's Sam Sites to target the Patrol Helicopter.

## Configuration

Default configuration:

```json
{
  "Debug rocket prediction": false,
  "Debug rocket damage": false,
  "NPC CH47 Helicopter": {
    "Can be targeted by static SAM Sites": true,
    "Targeting range": 150.0,
    "Rocket speed multiplier": 1.0,
    "Rocket damage multiplier": 8.0,
    "Seconds between rocket bursts": 5.0
  },
  "Player CH47 Helicopter": {
    "Can be targeted by static SAM Sites": true,
    "Targeting range": 150.0,
    "Rocket speed multiplier": 1.0,
    "Rocket damage multiplier": 2.0,
    "Seconds between rocket bursts": 5.0
  },
  "Patrol Helicopter": {
    "Can be targeted by static SAM Sites": true,
    "Targeting range": 150.0,
    "Rocket speed multiplier": 1.5,
    "Rocket damage multiplier": 8.0,
    "Seconds between rocket bursts": 5.0
  }
}
```

- `Debug rocket prediction` (`true` or `false`) -- Determines whether to show rocket trajectory to nearby admins.
- `Debug rocket damage` (`true` or `false`) -- Determines whether to show rocket damage on each hit to nearby admins.
- `Can be targeted by static SAM Sites` (`true` or `false`) -- Determines whether each type of helicopter can be targeted by static Sam Sites (e.g., by monument Sam Sites).
- `Targeting range` -- Determines how far away Sam Sites can target each type of helicopter.
  - In vanilla, Sam Sites have a targeting range of `150.0` for vehicles, and `225.0` for MLRS rockets.
- `Rocket speed multiplier` -- Determines how quickly Sam Site rockets will travel when fired at each type of helicopter.
  - In vanilla, rockets fired at vehicles use `1.0`, while rockets fired at MLRS rockets use `2.25`.
  - Default for `Patrol Helicopter` is `1.5` to deal with the fact that it can change directly quickly.
- `Rocket damage multiplier` -- Determines how much to multiply Sam Site rocket damage against each type of helicopter.
  - Default for `NPC CH47 Helicopter` is `8.0` which causes Sam Site rockets to deal `200` damage each, requiring a total of `20` rockets to destroy one heli (`4000` HP).
  - Default for `Player CH47 Helicopter` is `2.0` which causes Sam Site rockets to deal `50` damage each, requiring a total of `20` rockets to destroy one heli (`1000` HP).
  - Default for `Patrol Helicopter` is `8.0` which causes Sam Site rockets to deal `200` damage each, requiring a toal of `50` rockets to destroy one heli (`10000` HP).
- `Seconds between rocket bursts` -- Determines how frequently Sam Sites can fire rocket bursts at each type of helicopter.
  - In vanilla, rocket burst delay is `5` seconds against vehicles and `3.5` seconds against MLRS rockets.

## Credits

- Whispers88 Co-Author
