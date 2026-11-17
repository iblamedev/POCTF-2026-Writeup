# The Hidden Path

| | |
|---|---|
| **Section** | wave 5 |
| **Category** | steganography |
| **Points** | 100 |

## Overview

Sixteen glyphs. One specimen sheet. Nothing out of place—or so it seems.

A type specimen page has surfaced, showcasing a collection of carefully arranged glyphs. Each looks ordinary enough on its own, but the differences between them may be more deliberate than they appear.

The page is a document, but the message isn't necessarily in the letters themselves.

## Solve

PDF structure steganography hiding content in unused object streams and `/ActualText` tags.

Decompressed PDF streams with `qpdf --qdf`, inspected non-rendering content streams, and extracted hidden vector font tokens.

### Recovered Token

```text
POCTF{████████████████}
```
