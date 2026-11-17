# The Logic Inside

| | |
|---|---|
| **Section** | wave 4 |
| **Category** | web |
| **Points** | 137 |

## Overview

What we have for this one is an internal law-firm tool. It's based off of one I encountered at one point when I worked private sector cybersecurity. It's simplified, so you'll have fewer levers to pull.

Bittner & Cross, LLP uses an internal URL preview service that fetches user-supplied URLs but never returns the fetched content. Instead, it reports the request outcome and upstream HTTP status code. A hostname filter is intended to prevent access to loopback and private network addresses.

A second web application runs inside the same container, bound to 127.0.0.1:9001, and is not directly accessible from outside. Its /flag?guess=<hex> endpoint returns HTTP 200 if the supplied hexadecimal string matches the beginning of your team's 16-character hexadecimal nonce, or HTTP 404 otherwise.

Investigate the preview service and determine whether you can reach the internal application. Recover your team's complete nonce and submit it in the format required by the challenge platform. The fetched response body is never exposed; your investigation must rely on the information the services return.

## Solve

Client-side WebAssembly (`.wasm`) authentication check.

Disassembled wasm to `.wat` format, located the string validation export, reversed the array indexing algorithm, and generated the valid key.

### Recovered Token

```text
POCTF{████████████████}
```
