# Health Is a Social Construct

| | |
|---|---|
| **Section** | wave 4 |
| **Category** | game hacking |
| **Points** | 138 |

## Overview

A 2D top-down shooter. Three rooms. The final room's boss has more HP than you'll ever chip through, and hits harder than you can absorb. It is not intended to be beaten by aim or by patience.

Beat it anyway. The math is stacked against you — so change the math.

Download the game for your OS and the tiny credentials bundle, put them in the same folder, launch. Your team's credentials auth you in and let the end screen mint your flag.

## Solve

Memory-injected player status in Godot game engine allowing infinite health and god mode.

Located health variable offset via scanmemory / cheat engine, froze player health to `999999`, and defeated the impossible boss.

### Recovered Token

```text
POCTF{████████████████}
```
