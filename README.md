## Features

- Allows Sam Sites to target CH47 Helicopters (Chinooks)
- Allows Sam Sites to target Patrol Helicopters
- Allows Patrol Helicopters to retaliate against Sam Sites

If you are looking to prevent Sam Sites from targeting your own Minicopters, Scrap Transport Helicopters, etc., then look for that feature in other plugins such as [SAM Site Authorization](https://umod.org/plugins/sam-site-authorization).

## Permissions

- `helisams.ch47.npc` -- Allows the player's Sam Sites to target the **NPC** CH47 Helicopters.
- `helisams.ch47.player` -- Allows the player's Sam Sites to target **player** CH47 Helicopters.
- `helisams.patrolheli` -- Allows the player's Sam Sites to target the Patrol Helicopter.

## Configuration

Default configuration:

```json
{
  "NPC CH47 Helicopter": {
    "Can be targeted by static Sam Sites": true,
    "Targeting range": 150.0,
    "Rocket speed multiplier": 1.0,
    "Rocket damage multiplier": 4.0,
    "Seconds between rocket bursts": 5.0
  },
  "Player CH47 Helicopter": {
    "Check cupboard auth": false,
    "Can be targeted by static Sam Sites": true,
    "Targeting range": 150.0,
    "Rocket speed multiplier": 1.0,
    "Rocket damage multiplier": 2.0,
    "Seconds between rocket bursts": 5.0
  },
  "Patrol Helicopter": {
    "Can retaliate against Sam Sites": false,
    "Can be targeted by static Sam Sites": true,
    "Targeting range": 150.0,
    "Rocket speed multiplier": 1.5,
    "Rocket damage multiplier": 4.0,
    "Seconds between rocket bursts": 5.0
  },
  "Debug rocket prediction": false,
  "Debug rocket damage": false
}
```

The following option is only available for the `Player CH47 Helicopter` section.

- `Check cupboard auth` (`true` or `false`) -- Determines whether player Sam Sites will ignore player CH47 helicopters when a player in the helicopter is authorized to the Sam Site's tool cupboard. While `true`, Sam Sites will function like in the [SAM Site Authorization](https://umod.org/plugins/sam-site-authorization) plugin.

The following option is only available for the `Patrol Helicopter` section.

- `Can retaliate against Sam Sites` (`true` or `false`) -- Determines whether the Patrol Helicopter can fire rockets back at Sam Sites.

The following options are available for all types of helicopters.

- `Can be targeted by static Sam Sites` (`true` or `false`) -- Determines whether each type of helicopter can be targeted by static Sam Sites (e.g., by monument Sam Sites).
- `Targeting range` -- Determines how far away Sam Sites can target each type of helicopter.
  - Vanilla targeting range is `150.0` against vehicles, and `225.0` against MLRS rockets.
- `Rocket speed multiplier` -- Determines how quickly Sam Site rockets will travel when fired at each type of helicopter.
  - Vanilla speed multiplier is `1.0` against vehicles, and `2.25` against MLRS rockets.
  - Default for `Patrol Helicopter` is `1.5` to deal with the fact that it can change direction quickly.
- `Rocket damage multiplier` -- Determines how much to multiply Sam Site rocket damage against each type of helicopter.
  - Default for `NPC CH47 Helicopter` is `4.0` which causes Sam Site rockets to deal `100` damage, requiring a total of `40` rockets to destroy one heli (`4000` HP).
  - Default for `Player CH47 Helicopter` is `2.0` which causes Sam Site rockets to deal `50` damage, requiring a total of `20` rockets to destroy one heli (`1000` HP).
  - Default for `Patrol Helicopter` is `4.0` which causes Sam Site rockets to deal `100` damage, requiring a total of `100` rockets to destroy one heli (`10000` HP).
- `Seconds between rocket bursts` -- Determines how frequently Sam Sites can fire rocket bursts at each type of helicopter.
  - Vanilla time between rocket bursts is `5` seconds against vehicles, and `3.5` seconds against MLRS rockets.

The following options are configured globally.

- `Debug rocket prediction` (`true` or `false`) -- Determines whether to show rocket trajectory to nearby admins.
- `Debug rocket damage` (`true` or `false`) -- Determines whether to show rocket damage on each hit to nearby admins.

## Credits

- Whispers88 Co-Author
