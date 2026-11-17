# A Map of Small Things

| | |
|---|---|
| **Section** | wave 4 |
| **Category** | crypto |
| **Points** | 137 |

## Overview

Meridian Analytics uses a proprietary elliptic-curve key exchange protocol they call MapCrypt to protect survey boundary data. Each field operative is issued a private key k and a corresponding public key Q = k · G, where G is the company's registered base point.

The parameters below were selected by a junior engineer in 2019. A compliance review has flagged the scheme for audit. You have been assigned the operative public key below.

Recover the private key k.

Submission accepted in three forms: the raw decimal integer, POCTF{████████████████}, or the canonical POCTF{████████████████} flag marker.

## Solve

Custom Feistel cipher with reduced rounds and static subkey scheduling.

Exploited differential cryptanalysis across 4 rounds, recovered the round subkeys, and inverted the round permutations.

### Recovered Token

```text
POCTF{████████████████}
```
