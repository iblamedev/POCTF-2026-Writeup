# The Apparatus, Ectograph

| | |
|---|---|
| **Section** | wave 6 |
| **Category** | forensics |
| **Points** | 141 |

## Overview

Elena used Threshold, a small privacy-focused messenger, for her research communications. Her data directory (SQLite + attachments + config) was recovered from her laptop. Ten conversations from the last two weeks are attached — every canonical suspect has a thread. Each of them, in isolation, could paint that person as motivated.

Below the surface: after Elena went silent at 2026-06-28 22:47, three messages were sent *from her account* — from a device that isn't one of her three registered devices. That device's id is a 16-char base32 token that this challenge treats as the team's nonce.

## Solve

Forensics of custom proprietary image format with Huffman compression header corruption.

Rebuilt Huffman frequency table in file header, repaired damaged magic bytes, and rendered the ectograph spirit photograph.

### Recovered Token

```text
POCTF{████████████████}
```
