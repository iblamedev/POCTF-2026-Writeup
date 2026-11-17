# An Invented Language

| | |
|---|---|
| **Section** | wave 4 |
| **Category** | reverse engineering |
| **Points** | 132 |

## Overview

Your team has recovered a small program written for an unfamiliar stack-based virtual machine. The archive contains program.iv, the reference interpreter ivmi.c, and a README with build and execution instructions.

Analyze the provided files to recover the program's hidden output and submit the flag in the format required by the challenge platform. You may approach the problem by executing the program or investigating its instruction set and behavior.

## Solve

Custom compiled dialect targeting an abstract stack machine with unique grammar tokens.

Wrote a lexer and parser for the invented grammar, reconstructed symbol tables, and traced variable assignments to extract the flag.

### Recovered Token

```text
POCTF{████████████████}
```
