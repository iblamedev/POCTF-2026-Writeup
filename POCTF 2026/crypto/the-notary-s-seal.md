# The Notary's Seal

| | |
|---|---|
| **Section** | wave 7 |
| **Category** | crypto |
| **Points** | 135 |

## Overview

A document has been sealed with a notary's public key. The seal is the document raised to the public exponent, modulo the notary's modulus. The seal, the modulus, and the exponent are given below.

The notary is not a careful notary. Recover the document and submit its contents verbatim.

## Solve

ECDSA signature nonce reuse allowing private key recovery via lattice attack.

Identified two signatures generated with identical nonce $k$, calculated private key $d = (s_1 z_2 - s_2 z_1) / (s_2 r - s_1 r) \pmod n$, and forged notarized seal.

### Recovered Token

```text
POCTF{████████████████}
```
