# A Quiet Home

| | |
|---|---|
| **Section** | wave 4 |
| **Category** | forensics |
| **Points** | 137 |

## Overview

Elena's apartment had a small HomeAssistant + Mosquitto MQTT stack
running mixed Z-Wave and Zigbee devices. On the Thursday she vanished
she was on campus all afternoon (device tracker at Hollis GPS). At
14:47 someone unlocked her front door using keypad slot 04 — a code
she had assigned to M. Halberd weeks earlier. There was motion in the
study until 15:34. Front door locked from inside at 15:36.

## Solve

Router firmware filesystem analysis (`squashfs`) containing hardcoded backdoor credentials.

Extracted firmware with `binwalk -Me`, inspected `/etc/shadow` and `/usr/bin/nvram`, finding the factory testing backdoors.

### Recovered Token

```text
POCTF{████████████████}
```
