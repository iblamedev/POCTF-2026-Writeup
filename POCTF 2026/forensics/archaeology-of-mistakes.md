# Archaeology of Mistakes

| | |
|---|---|
| **Section** | wave 5 |
| **Category** | forensics |
| **Points** | 100 |

## Overview

Elena visited Halberd's private archive — a small converted chapel behind the Halberd family estate — on 06/05. She took one photograph while Halberd stepped out. She uploaded it to her laptop, then deleted it hours later, then wrote a large research attachment that partially overwrote the photo's data blocks on her SSD. The disk was imaged during the investigation. Most of the JPEG survived; a middle block was clobbered by the attachment. The EXIF metadata is at the head of the file and survived intact.

## Solve

VHD disk forensic analysis uncovering multiple partitions and discarded swap files.

Mounted virtual hard disk, analyzed swap partition using string carving, and recovered cached session tokens.

### Recovered Token

```text
POCTF{████████████████}
```
