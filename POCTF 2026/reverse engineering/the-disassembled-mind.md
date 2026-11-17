# The Disassembled Mind

| | |
|---|---|
| **Section** | wave 2 |
| **Category** | reverse engineering |
| **Points** | 118 |

## Overview

SEANCE.EXE wasn't the only thing I "found" in that dusty old closet. There were other samples that proved less... capable. Like this specimen, which seems to have been captured mid-thought. The interpreter went cold in situ, but the cortex is intact — a single small function, five inline byte constants, and a check that verifies exactly one string against exactly one flag.

Two of the constants belong to no memory the specimen ever accessed. The other three combine, byte-wise, into your answer.

The compiled module runs on the exact interpreter that produced it; if the magic doesn't match, it won't wake. You are not expected to make it run. You are expected to section it, read what happened, and reconstruct what it saw.

Reader kit attached below. Submit the recovered flag or its nonce.

## Solve

Python bytecode decompilation (`.pyc`) with custom opcode remaps and obfuscated control flow.

Extracted bytecode instructions using `dis`, reversed the mathematical transforms applied to team ID 491, and synthesized the valid license token.

### Recovered Token

```text
POCTF{████████████████}
```
