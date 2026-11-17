# Velocity

| | |
|---|---|
| **Section** | wave 4 |
| **Category** | steganography |
| **Points** | 137 |

## Overview

An étude sketch containing 64 notes over approximately 30 seconds, composed in C major. However, each note provides a little bit of information that you'll need to solve the challenge. Your goal is to recover your team's 16-character hexadecimal nonce by examining the MIDI data and decoding the 64 bits in order, with each group of four bits representing one hexadecimal digit. Submit the recovered nonce, or the full flag.

## Solve

MIDI file velocity byte modulation encoding ASCII text into piano keypress velocities.

Parsed MIDI tracks using `mido`, extracted note velocity values `(event.velocity)`, converted integers to ASCII chars.

### Recovered Token

```text
POCTF{████████████████}
```
