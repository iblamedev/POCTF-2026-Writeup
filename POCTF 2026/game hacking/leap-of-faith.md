# Leap of Faith

| | |
|---|---|
| **Section** | wave 2 |
| **Category** | game hacking |
| **Points** | 87 |

## Overview

Games are just numbers pretending to be physics. One of those numbers is the height of your jump. In this case, that number is not quite high enough to reach the last platform. That is the point.

Download the game for your OS and the tiny credentials bundle, put them in the same folder, and launch. Your team's credentials auth you in and mint the flag if you can make it through the hoop!

NOTE: An error in this challenge led to the wrong game version being uploaded. The test binary trivializes the challenge. I have left the incorrect binary in place to keep the contest fair, but if you would like to try the challenge as it was designed and intended, you can <a href="https://uwspedu-my.sharepoint.com/:f:/g/personal/cjohnson_uwsp_edu/IgC_PM03cS64RLNiQeEQBi81AcO3U3A2i4r4k-9v5kfJFS0?e=ha0ivT">game bins from here.</a>

## Solve

Client-side movement physics manipulated via memory patching or modified game coordinates in a Godot jump game.

Intercepted player velocity vectors, modified jump impulse from `300.0` to `3000.0`, jumping directly onto the out-of-bounds floating flag platform.

### Recovered Token

```text
POCTF{████████████████}
```
