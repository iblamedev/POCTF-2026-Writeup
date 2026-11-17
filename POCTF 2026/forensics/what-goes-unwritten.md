# What Goes Unwritten

| | |
|---|---|
| **Section** | wave 3 |
| **Category** | forensics |
| **Points** | 120 |

## Overview

Elena used a Hollis public library workstation on 06/28 (Friday) to search for the LSSF's eighth session — a session that does not appear in any archive. Windows 10 22H2, Firefox 119. She read a paper on an academic mirror. She saved nothing, downloaded nothing. The library's end-of-session script force-terminated Firefox and captured a Windows minidump per IT policy. That dump made it into evidence.

Recover a 16-character base32 token (A-Z, 2-7) from the dump. Submit it directly (no POCTF{...} wrapper required).

## Solve

Memory dump forensics containing unallocated notepad memory and process heap strings.

Used Volatility 3 `windows.cmdline` and `windows.memdump`, grepped for draft memory buffers, and recovered the unsaved text editor session.

### Recovered Token

```text
POCTF{████████████████}
```
