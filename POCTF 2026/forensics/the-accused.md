# The Accused

| | |
|---|---|
| **Section** | wave 8 |
| **Category** | forensics |
| **Points** | 141 |

## Overview

Elena Marchetti disappeared on the night of 2026-06-28. Your intercept unit pulled three artifacts from the investigation window:

Marion Halberd’s Meridian Circle outbox for 06/28-06/30
A partial capture of /var/log/apparatus/ from the controller at Halberd’s estate, including a fragment of /etc/passwd
A plaintext telnet session recorded from inside the estate network late on 06/28

The sessions directory contains more than one log, with opaque operator codes and subject codes — no names. Figure out which session is Elena’s and who ran it.

Submit the 16-character session_id of that log and an accusation naming the operator.

CHOOSE CAREFULLY. YOU ONLY GET ONE SHOT. You must find the flag AND solve the case correctly to earn points for this challenge!!

## Solve

Windows memory forensics of `marchetti-2026-14` process examining encrypted DPAPI credentials and SQLite database history.

Extracted user DPAPI master key, decrypted local state database, and pulled the encrypted conversation logs detailing the accused's actions.

### Recovered Token

```text
POCTF{████████████████}
```
