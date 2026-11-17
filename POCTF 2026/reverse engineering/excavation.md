# Excavation

| | |
|---|---|
| **Section** | wave 1 |
| **Category** | reverse engineering |
| **Points** | 122 |

## Overview

I tell you, the game hacking category was a lot of fun to develop over summer. Unfortunately, not all ideas make the cut. Take this game, for example. Here are some remnants of the fictional dark-fantasy RPG "Sepulchure of the Undying". I had high hopes, but I suffered a hardware failure and *poof* it's all gone. All I could save were a few save files from testing. Oh, well. When life gives you lemons, reverse engineer the file format and find a flag.

Remember: The flag for this challenge is a little different. You're looking for a 16 character token.

## Solve

Reverse engineering legacy save-state binary structures (`.sav`) with XOR-scrambled player progress arrays.

Compared sample `.sav` files, located the team-specific high-score block at offset `0x180`, unscrambled the 16-character token via XOR differential analysis.

### Recovered Token

```text
POCTF{████████████████}
```
