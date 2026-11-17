# Commit to Memory

| | |
|---|---|
| **Section** | wave 2 |
| **Category** | steganography |
| **Points** | 128 |

## Overview

I had an idea for a complex Reverse challenge using live GitHubs that didn't quite work out. What we have here is sort-of based on that idea. 

The conciet: A researcher exported a side project as a git bundle. Two files, roughly 55 commits, all of it aggressively unremarkable. The README is a stub. The CHANGELOG grows one line per commit. The commit messages are the boring vocabulary of routine housekeeping: "fix typo," "bump patch," "reformat with black."

grep -r POCTF returns nothing. strings on every blob returns nothing. And yet the flag is there.

## Solve

Git bundle history containing dangling commits and stashed credentials.

Cloned the git bundle, ran `git fsck --lost-found`, recovered unreferenced dangling commit blobs, and retrieved the committed secret.

### Recovered Token

```text
POCTF{████████████████}
```
