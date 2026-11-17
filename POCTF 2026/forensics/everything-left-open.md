# Everything Left Open

| | |
|---|---|
| **Section** | wave 1 |
| **Category** | forensics |
| **Points** | 67 |

## Overview

You've got no idea what you've gotten yourself into, Gumshoe. You think this is just a quick little peak at some secrets, collect a payday, and move on with your life, huh? Well, we'll just see about that. Could be this is just the first step. Better wise up, flatfoot.

A hotel security officer bagged a laptop a guest walked away from —
still unlocked, browser open, data entered mid-form. It was zipped up by an outside IT consulting firm the hotel retained, how it's in your hands. There a flag in that session, but you might want to pay attention to the details, just in case.

## Solve

Unencrypted network capture (`pcap`) containing cleartext HTTP credentials and Telnet session handshakes.

Loaded the pcap into Wireshark / tshark, followed the TCP stream on port 23, and extracted the authenticated admin session token.

### Recovered Token

```text
POCTF{████████████████}
```
