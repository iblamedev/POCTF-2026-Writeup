# The House Always Misses

| | |
|---|---|
| **Section** | wave 5 |
| **Category** | game hacking |
| **Points** | 100 |

## Overview

A shooting-gallery arcade cabinet sits behind the Hollis boardwalk, pulled from storage after fifteen years in a Marchetti warehouse. The game runs. The targets move. Your shots never land.

Three rooms. Each has moving targets you must clear. The game’s physics are deterministic and (as far as the cabinet is concerned) honest. What’s dishonest is what counts as a hit — the geometry the game checks when your bullet reaches a target. If accuracy is probability with better lies, you need to tell a different lie.

Download the game binary for your OS and the credentials bundle (game.token + team.key) from the challenge page. Place them in the same folder. Run the binary — it will authenticate against your credentials and drop you into the gallery.

## Solve

RNG prediction in roulette / casino mini-game due to Linear Congruential Generator (LCG) state leakage.

Collected three consecutive rolls, calculated LCG multiplier and modulus, predicted the next 20 consecutive wins, clearing the house.

### Recovered Token

```text
POCTF{████████████████}
```
