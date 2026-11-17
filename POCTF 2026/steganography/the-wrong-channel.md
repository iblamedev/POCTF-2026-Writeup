# The Wrong Channel

| | |
|---|---|
| **Section** | wave 6 |
| **Category** | steganography |
| **Points** | 141 |

## Overview

A PNG. Nothing extraordinary at first glance. The usual LSB-stego checks will light up — the lowest-order bits of the red, green, and blue channels are noisy enough that your tool of choice will insist it's found something: a hidden message, a key, maybe a watermark.

It hasn't. The real payload lives in a different place. Find it.

## Solve

Alpha channel PNG steganography hiding high-entropy ciphertext in transparent pixel components.

Isolated the 8-bit Alpha channel using PIL, discarded RGB layers, and decoded the hidden grayscale ASCII barcode.

### Recovered Token

```text
POCTF{████████████████}
```
