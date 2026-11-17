# Invisible Ink

| | |
|---|---|
| **Section** | wave 1 |
| **Category** | steganography |
| **Points** | 113 |

## Overview

Humans are the dominant species on the planet. No question. How did we get that way? Because we're smarter? Because we can run longer? Those things might be true - but not for a long time after we're born. We'd never survive to adulthood if those were our main gifts. 

No, our main survival trait is exactly what babies are best known for: Crying. Communicating. And we have found millions of ways to do it. Languages, written words, radio, TV, walkie talkies, morse code, ASL... There's just no shutting us up. We communicate, we band together, and we survive. We don't, we die.

But not all messages are broadcast for the world to see. Some secrets need to be kept, and keeping them is an art. In this challenge I have a hidden message. It's not difficult to work out, but I'm confident you'll see what I'm communicating if you look in the right place.

## Solve

Zero-width unicode character steganography hidden within plain text python script docstrings.

Extracted invisible zero-width spaces (`​`, `‌`, `‍`), converted them to binary bits (0 and 1), and decoded ASCII text to recover the flag.

### Recovered Token

```text
POCTF{████████████████}
```
