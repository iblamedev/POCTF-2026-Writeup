# The State of Trust

| | |
|---|---|
| **Section** | wave 8 |
| **Category** | web |
| **Points** | 141 |

## Overview

The Bureau of Trust issues identity tokens via its OAuth 2.0 authorization service. Administrator accounts are issued through internal channels only — but the Bureau is, in fact, hiring a new auditor for its trust-seal system.

## Solve

OAuth2 / Session State Parameter Validation Bypass in Python Flask web app.

Discovered source code backup `source.py.bak`, found flawed HMAC state verification accepting unsigned user IDs, spoofed `user_id=1` (Admin) in OAuth callback.

### Recovered Token

```text
POCTF{████████████████}
```
