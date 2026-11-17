# A Cabin Worth

| | |
|---|---|
| **Section** | wave 2 |
| **Category** | forensics |
| **Points** | 119 |

## Overview

Well, looks like you stepped in it this time, Gumshoe. You thought you had a simple job and now you're in the middle of a disappearance. Elena M. What's clear is that -someone- doesn't want her found. Maybe she ran off on her own because she couldn't take the pressure, but the fact that someone is trying to cover their tracks means you better be ready for anything. 

Someone deleted the evidence.

Or at least, that's what the database says.

You're given a SQLite database that appears to be clean—but databases have memories, and sometimes the past lingers in places nobody thought to check.

If something was deleted, where did it go before it was truly gone?

Dig into the database's supporting files and see what the application forgot to forget.

## Solve

Deleted file recovery from a corrupted FAT32 image of an offline logger.

Parsed FAT directory tables, reconstructed orphaned clusters from unallocated slack space, and carved the deleted PNG log file containing the flag.

### Recovered Token

```text
POCTF{████████████████}
```
