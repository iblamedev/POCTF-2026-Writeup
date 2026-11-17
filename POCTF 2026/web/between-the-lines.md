# Between the Lines

| | |
|---|---|
| **Section** | wave 7 |
| **Category** | web |
| **Points** | 139 |

## Overview

A reverse proxy sits in front of an application server. The two don’t quite agree on how an HTTP/1.1 request ends. Exploit the disagreement to reach an endpoint the proxy pretends doesn’t exist.

## Solve

HTTP Request Smuggling via TE.CL desynchronization in reverse proxy.

Sent smuggled chunked request prefixing second internal request to `/admin/flag`, capturing the administrative response.

### Recovered Token

```text
POCTF{████████████████}
```
