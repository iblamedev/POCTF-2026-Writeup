# The Apparatus, Dissolution

| | |
|---|---|
| **Section** | wave 7 |
| **Category** | reverse engineering |
| **Points** | 140 |

## Overview

The Threshold’s junior operators were taught that no signal leaves a session uncompensated. Everything the Apparatus emitted was dissolved through the operator’s own cipher — four passes — before it left the room.

This workstation ran one last dissolution the night its operator vanished. The source is still on the drive. The dissolved output is written into the source. What entered the instrument is not.

Recover it.

## Solve

Self-modifying x86-64 binary decrypting instructions dynamically on the stack before execution.

Set execution hardware watchpoints in GDB, dumped decrypted opcode buffers immediately prior to execution, and reconstructed the key generator.

### Recovered Token

```text
POCTF{████████████████}
```
