# The Oracle's Weight

| | |
|---|---|
| **Section** | wave 5 |
| **Category** | reverse engineering |
| **Points** | 140 |

## Overview

An oracle sits behind a door. It accepts an 8-element vector of floats in [0,1] and returns a single scalar. For almost every input it returns a value near 0. For exactly one input — your team's 8-byte key, normalised by dividing each byte by 255 — it returns a value near 1.

The door is open. The oracle is a trained neural network, shipped as a standard ONNX file. Find the input that drives its output above 0.75.

Submit the 16 lowercase hex characters of the 8 bytes you find. The server will run the oracle on your submission to verify.

What you need: an ML framework that can load ONNX and run gradient-based optimisation on the input (PyTorch via onnx2torch, or a direct reimplementation of three Dense layers + LeakyReLU in NumPy with analytic gradients).

What won't work: reading the weights expecting the key to be sitting in a column. Random guessing (2^64 search space). Running the model forward with random inputs (random inputs score near 0).

## Solve

ONNX deep neural network weight extraction and feature map inversion.

Extracted tensor weights from `oracle.onnx`, inverted the classification activation layer using gradient descent, reconstructing the input image flag.

### Recovered Token

```text
POCTF{████████████████}
```
