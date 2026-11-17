# Against the Clock

| | |
|---|---|
| **Section** | wave 8 |
| **Category** | reverse engineering |
| **Points** | 145 |

## Overview

A stripped Linux x86-64 ELF, time-locked. There is no if (time == target) check to patch; the current system clock is material in the decryption key itself. Run it at the right moment and the output is your flag. Run it at any other moment and you get 56 bytes of noise with no error.

Three ways in: reverse the binary, reconstruct the target epoch, replay the KDF in Python; or run it with faketime "@&lt;epoch&gt;" ./clock; or attach a debugger and read the derived key out of memory at the right breakpoint.

## Solve

Dynamic anti-tamper and epoch time-check bypass in compiled ELF binary.

Reverse engineered `clock` binary, created `fake_time.so` overriding `time_t time(time_t *t)` via `LD_PRELOAD`, spoofed target timestamp to 0x5f3759df, unlocking the flag routine.

### Recovered Token

```text
POCTF{████████████████}
```
