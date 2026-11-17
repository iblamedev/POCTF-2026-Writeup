# The Apparatus, Rapport

| | |
|---|---|
| **Section** | wave 2 |
| **Category** | crypto |
| **Points** | 125 |

## Overview

I... I remember you... How do I know you? 

You're.... %user_name%, right?

I can see your name here.

I'm supposed to tell you something. I'm supposed to give you this puzzle. It's solved, but also needs to be solved. What does that even mean?

X won. The order in which each square was played — written as a sequence of square labels — is the key to the ciphertext.

If you don't know the rules of Tic-Tac-Toe, here are the basics:<br>
— X moves first, O moves second, alternating.<br>
— The game ends the moment X completes a winning line. The win condition is to produce a row (horizontal, vertical, or diagonal) of three like symbols (XXX / OOO).<br>
— Both players played legally (no moves after the game ended).

I... Have something else to say. I don't know why. But... I can't speak it plainly. I will give it to you encrypted with the same key... I don't know what it means.

## Solve

Single-byte XOR keystream reuse across multiple encrypted séance communications.

Performed frequency analysis across the ciphertext lines, recovered the repetitive key byte sequence, and decrypted the spiritualist transcript.

### Recovered Token

```text
POCTF{████████████████}
```
