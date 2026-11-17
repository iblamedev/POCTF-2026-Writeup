# Client-Side Truth

| | |
|---|---|
| **Section** | wave 8 |
| **Category** | game hacking |
| **Points** | 141 |

## Overview

For the final GH challlenge this year, I took several of the earlier games and rolled them all up into a new design. We've got the verticality of 1. The shooter design of 2 (but now in 3D!), the targeting of 3, and the big boss mechanic of 4. And this time I made sure to do it RIGHT! Server-authoritative processing. SURELY this game is 100% SEC-UR. Except, maybe I forgot that if the client decides what's true, the client can lie.

## Solve

Godot 3D game engine client-authoritative network validation flaw.

Decompiled `game.pck`, analyzed `FlagToken.gdc` bytecode, extracted the client-side validation logic and decryption key, and minted the valid submission token.

### Recovered Token

```text
POCTF{████████████████}
```
