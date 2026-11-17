# No Structure Required

| | |
|---|---|
| **Section** | wave 3 |
| **Category** | web |
| **Points** | 109 |

## Overview

SecureNotes v1.0 — a small internal notes platform from a vendor that's long since folded. The staff left behind a login screen, a browse page, and a collection of records they thought they'd deleted.

There's an entry in there your team is supposed to see. It's not in the obvious places.

Credentials? You weren't issued any. See what the login accepts.

## Solve

NoSQL injection in MongoDB JSON endpoint allowing authentication bypass via `{"$ne": null}`.

Submitted `{"username": "admin", "password": {"$regex": "^p.*"}}`, iteratively leaked admin token using regex queries.

### Recovered Token

```text
POCTF{████████████████}
```
