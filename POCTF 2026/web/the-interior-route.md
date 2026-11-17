# The Interior Route

| | |
|---|---|
| **Section** | wave 6 |
| **Category** | web |
| **Points** | 141 |

## Overview

A URL-preview service — the kind blogs embed to render shared links. Paste a URL, the server fetches it, a snippet of the response comes back. The service is public, trusts user input, and runs on infrastructure provisioned "the standard way."

The preview service only returns what it can fetch from external hosts. It cannot reach any private network. (It swears.)

Your flag is sitting on something the preview service shouldn't be able to see.

## Solve

Server-Side Request Forgery (SSRF) accessing internal cloud metadata service (`169.254.169.254`).

Passed encoded internal IP payload to image fetcher, requested `http://169.254.169.254/latest/meta-data/iam/security-credentials/`, leaking admin role.

### Recovered Token

```text
POCTF{████████████████}
```
