# Interface Sketches
## General Ideas
- monospace font
- game server + (independent) UI layer
    - JSON API between server and client
    - results in more implementation possibilities, e.g. terminal, web, mobile
    - community provides more stories/mods/clients/skins/...
    - multiplayer?! (voting for next choice, group-based battle)
- music + sound fx (simple 8 bit stuff)
- shake feedback (e.g. during surprise traps and attacks)?
- who writes the story?


## Box UI Style
- See https://www.wikiwand.com/en/Box-drawing_character
- width: 32 chars?

```
┎──────────────┐┎──────────────┐
│ Bat          ││ You          │
│ HP:  9/12    ││ HP: 30/92    │
│ MP: -        ││ MP: 12/27    │
└──────────────┘└──────────────┘
┎──────────────────────────────┐
│ ○ Attack                     │
│ ● Magic                      │
│ ○ Items                      │
│ ○ Escape                     │
└──────────────────────────────┘
```


## Purely Text-based
- more action and excitement!
- width: 48 chars?
- colors?
- 3 choices per part/chapter/...
- doesn't need to be medieval or something (modern setting could be very refreshing!)

### Story Mode
```
You wake up in a dark cave. Beside you lays a torch on the ground that lights up the stoney walls closeby. Some water is dripping from the ceiling and splashing into a little puddle near your face. Your legs feel very weak — in fact you can barely feel them.

▸ Try to get up
  Grab the torch
  Shout for help
```

### Battle Mode
```
Starting a fight with Bat!
You hit Bat! It lost 3 HP.
Bat used "Wingflap"! You lost 1 HP.
---
Bat:  9/12 HP ・     - MP
You: 30/92 HP ・ 12/27 MP

You used "Heal" (2 MP). You gained 12 HP.
Bat used "Bite"! You lost 2 HP and are now poisoned.
---
Bat:  9/12 HP ・     - MP
You: 40/92 HP ・ 10/27 MP ・ poisoned
────────────────────────────────────────────────
  Attack   ▸ Fireball (5 MP)
▹ Magic      Heal     (2 MP)
  Items       
  Dodge      
  Escape     
```

### Story Mode (Multiplayer)
- every player has a symbol (▸, ▪︎, ◆) and players can see the choices of the other players (live update)
```
There will be some story part here.

  ▸ Do this
    Do that
▪︎◆  Do another thing
```

# Inspiration
- [WarriorJS](https://warrior.js.org)
