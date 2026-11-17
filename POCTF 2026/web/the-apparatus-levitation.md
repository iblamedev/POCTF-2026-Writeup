# The Apparatus, Levitation

| | |
|---|---|
| **Section** | wave 5 |
| **Category** | web |
| **Points** | 100 |

## Overview

The Liminal Society for Spectral Fellowship maintains a private parlour portal at levitation.pointeroverflowctf.com where mediums may attend recorded sittings.

Present your team's session token, open a MEDIUM-role session, and attempt to access the SPIRIT-only transcripts. The token you use is issued below, expiring fifteen minutes after this page loads.

Only SPIRIT-role subscribers may recover the marker embedded in the transcript. MEDIUMS may read only their own attendance record.

## Solve

IDOR and session role privilege escalation in private séance portal.

Manipulated JWT claims or session roles from `MEDIUM` to `SPIRIT`, accessing the restricted spiritualist transcripts.

### Recovered Token

```text
POCTF{████████████████}
```
