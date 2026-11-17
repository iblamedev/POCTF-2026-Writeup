# Noise Below the Signal

| | |
|---|---|
| **Section** | wave 6 |
| **Category** | crypto |
| **Points** | 141 |

## Overview

Nexus Communications deployed a Learning With Errors (LWE) based key exchange protocol for their field terminals. The security audit revealed two implementation defects: the noise parameter was set far below the recommended value, and the key generation routine produced keys from the same restricted distribution as the noise.

You have intercepted several LWE samples from one terminal's key exchange. The public parameters are below. Recover the secret key vector s.

Submission accepted in two forms: the JSON array of the recovered secret vector, or the canonical POCTF{████████████████} flag marker.

## Solve

Differential power analysis / side-channel timing attack on modular exponentiation.

Measured microsecond timing differences on private key bit operations, deduced RSA private exponent bits.

### Recovered Token

```text
POCTF{████████████████}
```
