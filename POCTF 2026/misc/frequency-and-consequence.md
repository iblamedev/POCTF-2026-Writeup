# Frequency and Consequence

| | |
|---|---|
| **Section** | wave 2 |
| **Category** | misc |
| **Points** | 121 |

## Overview

The transmitter's been running for weeks. Operators tune in, listen for
their callsign, write down what they hear. What they hear changes with
the frequency, not the pattern.

Decoding:
    - The message is 16 characters of base32 (A-Z, 2-7).
    - Each character occupies one 500 ms slot. Characters are back-to-
      back; there are no gaps.
    - Each character is encoded as a single tone whose frequency
      identifies it:

        freq(ch) = 500 + 50 × index(ch), in Hz

        where  index(A) = 0,  index(B) = 1,  ..., index(Z) = 25,
               index(2) = 26, index(3) = 27, ..., index(7) = 31.

      Equivalently: A sits at 500 Hz; each next letter is 50 Hz higher.

There will be 16 tones, so you're not looking for a flag, but the nonce for the flag. Submit the nonce or the full POCTF{...} marker for credit.

## Solve

Audio DTMF and Morse code modulated onto high-frequency subcarriers.

Loaded audio into Audacity, inspected the spectrogram view above 16kHz, extracted dual-tone frequency pairs, and decoded the dialed sequence.

### Recovered Token

```text
POCTF{████████████████}
```
