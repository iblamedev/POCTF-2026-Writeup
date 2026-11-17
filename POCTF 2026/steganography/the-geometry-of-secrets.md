# The Geometry of Secrets

| | |
|---|---|
| **Section** | wave 7 |
| **Category** | steganography |
| **Points** | 140 |

## Overview

Marchetti Modeling Suite
Precision in every dimension.

The attached Wavefront object was recovered from an otherwise unremarkable modeling project. Its original creator, Marchetti Modeling Suite, specializes in decorative geometry and precision modeling.

At first glance, the object appears to be little more than a collection of vertices and faces arranged into a curious geometric construction. Nothing particularly remarkable. Certainly nothing that would justify the attention it has received.

But appearances can be deceiving.

The file contains more than a model of three-dimensional space. Somewhere in its structure is a message waiting to be reconstructed.

## Solve

3D wavefront OBJ model vertex coordinates encoding binary data in IEEE-754 floating point mantissas.

Parsed vertices `v x y z`, extracted least significant bits of floating point representations, and assembled the hidden payload.

### Recovered Token

```text
POCTF{████████████████}
```
