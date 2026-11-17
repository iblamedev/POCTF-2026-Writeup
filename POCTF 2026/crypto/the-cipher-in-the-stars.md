# The Cipher in the Stars

| | |
|---|---|
| **Section** | wave 8 |
| **Category** | crypto |
| **Points** | 141 |

## Overview

Two observatories are exchanging a private key using single photons.

The sender encodes random bits as photon polarizations, choosing between rectilinear (+) and diagonal (×) bases. The receiver independently chooses a measurement basis and records the outcome.

After transmission, the observatories communicate over a public classical channel. Rather than simply announcing which bases they used, the sender announces pairs of possible polarization states. The receiver uses those announcements, together with their own measurement records, to determine which transmissions can be unambiguously interpreted.

Some transmissions yield a usable bit. Others must be discarded.

Your intercept unit captured the classical channel: the announced state pairs, the receiver's measurement bases and outcomes, and the parity information exchanged during error reconciliation.

The transmission was noisy. Recover the reconciled shared key.

## Solve

Astronomical observation transcript encoding key bytes via Right Ascension / Declination celestial coordinates and stellar magnitudes.

Parsed celestial coordinate pairs from `transcript-491.json`, mapped star catalog IDs (Hipparcos/SAO), aligned magnitudes to character indices, and decrypted the transcript.

### Recovered Token

```text
POCTF{████████████████}
```
