# The Oxidized Archive

| | |
|---|---|
| **Section** | wave 6 |
| **Category** | reverse engineering |
| **Points** | 145 |

## Overview

A Marchetti-era Rust utility. Builds and runs on any modern toolchain and reads no input — in principle it recovers an archive and prints its contents. In practice it prints nothing, because the archive and the key that unlocks it both travel inside the binary, and the author's "crypto" was not actually crypto.

Source and build instructions are in the download. The flag is the plaintext the utility ought to be printing.

## Solve

Reverse engineering Rust binary (`oxidized-archive`) with complex iterators and closures.

Symbolicated Rust mangled names using `rustfilt`, decompiled encryption state machine, and reversed the bitwise transformation.

### Recovered Token

```text
POCTF{████████████████}
```
