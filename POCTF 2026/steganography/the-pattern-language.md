# The Pattern Language

| | |
|---|---|
| **Section** | wave 8 |
| **Category** | steganography |
| **Points** | 100 |

## Overview

A plaid swatch. It’s not a flag, but it’s in there somewhere.
The weave is honest. Inspect it like you’d inspect anything else.
Deagh fhortan leis an t-sealg agad.

## Solve

Spatial pixel matrix steganography with Conway Life pattern grid overlaid onto RGB color planes.

Extracted least significant bit from green and blue channels of `pattern-491.png`, assembled 2D matrix, ran inverse Life transition rules to read token.

### Recovered Token

```text
POCTF{████████████████}
```
