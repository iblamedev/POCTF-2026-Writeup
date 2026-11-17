# Poisoned Well

| | |
|---|---|
| **Section** | wave 2 |
| **Category** | web |
| **Points** | 95 |

## Overview

There's nothing quite like a newspaper that can't stop repeating itself.

The Daily Whatever sits behind a response cache. Pages are supposed to be fast, consistent, and identical for everyone.

Supposed to be.

Somewhere between the request and the response, the cache is making assumptions.

Figure out what it trusts, what it remembers, and how to make it remember the wrong thing.

## Solve

Server-Side Template Injection (SSTI) in Jinja2 template rendering user greeting.

Payload `{{ cycler.__init__.__globals__.os.popen('cat flag.txt').read() }}` executed arbitrary commands on the web server, returning the flag.

### Recovered Token

```text
POCTF{████████████████}
```
