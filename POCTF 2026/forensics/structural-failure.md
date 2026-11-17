# Structural Failure

| | |
|---|---|
| **Section** | wave 7 |
| **Category** | forensics |
| **Points** | 140 |

## Overview

Elena obtained a Meridian Circle correspondence archive via
F. Delacroix on 06/22. She kept it as a ZIP on her laptop. Someone
attempted to destroy the archive by mangling the ZIP's tail
structures — the End-of-Central-Directory record and every
central directory entry are overwritten with garbage. The local
file headers and the compressed streams above them are intact.

Recover the archive. Read all three files. Elena's docket
reference in her annotations is the token.

## Solve

Zip archive corruption with malformed Central Directory records and CRC mismatches.

Repaired zip headers, aligned End of Central Directory (EOCD) offset, unpacked inner archive, and extracted sensitive logs.

### Recovered Token

```text
POCTF{████████████████}
```
