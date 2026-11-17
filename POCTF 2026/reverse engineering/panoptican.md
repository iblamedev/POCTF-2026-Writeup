# Panoptican

| | |
|---|---|
| **Section** | wave 3 |
| **Category** | reverse engineering |
| **Points** | 112 |

## Overview

Panoptican Biometric Solutions, Inc. shipped sealed verification binaries to municipal clients in the mid-2010s. Each binary was pre-enrolled with a single reference identity — if a submitted photograph matched the enrolled subject, the system printed an authorization code. Panoptican went bankrupt in 2019. One of their binaries ended up in your hands.

Figure out whose face is enrolled, and what the authorization code is.

## Solve

Multi-threaded surveillance binary with anti-debugging and ptrace detection.

Patched `ptrace` system call return values in GDB, bypassed timing checks (`rdtsc`), and extracted the decrypted telemetry flag.

### Recovered Token

```text
POCTF{████████████████}
```
