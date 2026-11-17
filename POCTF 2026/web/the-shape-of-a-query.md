# The Shape of a Query

| | |
|---|---|
| **Section** | wave 1 |
| **Category** | web |
| **Points** | 97 |

## Overview

Progress relies on having the right infrastructure to foster collaboration. A frictionless system for the exchange of ideas, integrity-preserving measures, and plenty of backup. There are many platforms on the market for this. Well, I'm developing my own. It's not the best. It's not the fastest. It's not the most resilient. But it is the one that I own the IP rights for, so I'm pushing it hard. Since I have a bevy of CTF player's attention, seems like a good chance to score some free pen testing. Head over to my Collaborative Research Portal and poke around a little. I am most concerned about user security. Last thing we need is for researchers to start meddling with each others' stuff.

## Solve

Blind SQL injection via Boolean-based query shaping in search parameter.

Injected `' OR (SELECT SUBSTRING(flag,1,1) FROM secrets)='p' --`, iterated across characters with a python requests script to dump the flag character by character.

### Recovered Token

```text
POCTF{████████████████}
```
