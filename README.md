# Pointer Overflow CTF 2026 — Official Write-ups

<p align="center">
  <img alt="Standing" src="https://img.shields.io/badge/Rank-%233%20Global%20Podium-2ea043?style=for-the-badge&logo=target&logoColor=white">
  <img alt="Solves" src="https://img.shields.io/badge/Solves-69%20%2F%2069%20(100%25)-9B59B6?style=for-the-badge&logo=checkmarx&logoColor=white">
  <img alt="Bracket" src="https://img.shields.io/badge/Bracket-Team%20(Top%203%20of%201931)-1f6feb?style=for-the-badge&logo=shield&logoColor=white">
  <img alt="Status" src="https://img.shields.io/badge/Speed%20Sweep-First%20Full%20Clear-f39c12?style=for-the-badge&logo=clockify&logoColor=white">
</p>

<p align="center">
  Complete technical write-ups, vulnerability analyses, reverse-engineering notes, and exploit scripts for <b>Pointer Overflow CTF 2026 (POCTF 2026)</b>.<br>
  Solved and documented by <b>iblamedev</b> in team <b>Don Quixote</b> (Team ID: <code>491</code>).
</p>

---

## Performance & Highlights

| Metric | Result | Description |
| :--- | :--- | :--- |
| **Global Standing** | **3rd Place Global Podium** | Finished #3 out of 425 teams in the Team Bracket (1,931 teams & 2,582 players overall) |
| **Total Solves** | **69 / 69** | **100% Full Board Clear** across all 8 released waves |
| **Speed Sweep** | **15:55:01 UTC** | First team across the global leaderboard to achieve a complete sweep of Wave 8 |
| **Total Points** | **8,567 pts** | Maximum available points on the challenge board |
| **Target URL** | [pointeroverflowctf.com](https://pointeroverflowctf.com) | Hosted by the University of Wisconsin–Stevens Point |

> [!NOTE]
> **Token & Flag Redaction Policy**: In accordance with CTF platform standards and anti-flag-sharing rules, all recovered challenge tokens and submission flags have been intentionally redacted (`POCTF{████████████████}`). Complete technical methodologies, mathematical derivations, decompiled logic, and exploit scripts are fully documented.

---

## Repository Structure

The challenges are organized into modular category directories matching standard CTF repository conventions:

```text
POCTF 2026/
├── crypto/                 # 8 Challenges (Vigenère, Matrix, Diffie-Hellman, Lattice, BB84 Quantum)
├── exploitation/           # 8 Challenges (Buffer overflows, ROP, Format strings, Heap exploitation)
├── forensics/              # 8 Challenges (PCAP extraction, Disk images, Corrupt media, Memory dump)
├── game hacking/           # 5 Challenges (Assembly patching, Memory scanning, Physics manipulation)
├── misc/                   # 8 Challenges (Esoteric runtimes, Audio frequency, Bytecode, Logic puzzles)
├── osint/                  # 8 Challenges (Geolocation, Metadata forensic recovery, Shadow tracking)
├── reverse engineering/    # 8 Challenges (x86_64 ELF reversing, Rust deobfuscation, Time-locked KDFs)
├── steganography/          # 8 Challenges (Least Significant Bit, Spatial patterns, Color channels)
└── web/                    # 8 Challenges (SQLi, SSTI, Prototype Pollution, JWT forgery, OAuth bypass)
```

---

## Challenge Index (69/69 Solved)

<details open>
<summary><b>Cryptography (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [Letters Never Sent](POCTF%202026/crypto/letters-never-sent.md) | 95 | Vigenère polyalphabetic cipher with occult letter key derivation |
| Wave 2 | [The Apparatus, Rapport](POCTF%202026/crypto/the-apparatus-rapport.md) | 125 | Matrix substitution cipher & modular arithmetic |
| Wave 3 | [The Consulting Room](POCTF%202026/crypto/the-consulting-room.md) | 125 | Playfair cipher variant with custom historical table |
| Wave 4 | [A Map of Small Things](POCTF%202026/crypto/a-map-of-small-things.md) | 137 | RSA small public exponent attack (Coppersmith theorem) |
| Wave 5 | [Forty Measures Deep](POCTF%202026/crypto/forty-measures-deep.md) | 100 | Dual-layer substitution & transposition decrypt |
| Wave 6 | [Noise Below the Signal](POCTF%202026/crypto/noise-below-the-signal.md) | 141 | Low-amplitude signal phase demodulation |
| Wave 7 | [The Notary's Seal](POCTF%202026/crypto/the-notary-s-seal.md) | 135 | ECDSA nonce reuse private key recovery |
| Wave 8 | [The Cipher in the Stars](POCTF%202026/crypto/the-cipher-in-the-stars.md) | 141 | BB84 quantum key exchange simulation & classical channel interception |

</details>

<details>
<summary><b>Binary Exploitation (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [Read Me My Fortune](POCTF%202026/exploitation/read-me-my-fortune.md) | 104 | Stack buffer overflow to ret2win |
| Wave 2 | [Thirty-Two Steps Down](POCTF%202026/exploitation/thirty-two-steps-down.md) | 128 | 32-bit integer truncation leading to out-of-bounds write |
| Wave 3 | [The Sandglass](POCTF%202026/exploitation/the-sandglass.md) | 98 | Time-of-check to time-of-use (TOCTOU) race condition |
| Wave 4 | [A Few Seconds Either Way](POCTF%202026/exploitation/a-few-seconds-either-way.md) | 133 | Format string vulnerability with `%n` arbitrary memory write |
| Wave 5 | [What the Heap Remembers](POCTF%202026/exploitation/what-the-heap-remembers.md) | 100 | Use-After-Free (UAF) chunk reuse exploit |
| Wave 6 | [The Interpreter's Margin](POCTF%202026/exploitation/the-interpreter-s-margin.md) | 141 | JIT bytecode compiler confusion leading to RCE |
| Wave 7 | [Permission Slip](POCTF%202026/exploitation/permission-slip.md) | 140 | Return-Oriented Programming (ROP) chain to bypass NX/DEP |
| Wave 8 | [The Apparatus, Manifestation](POCTF%202026/exploitation/the-apparatus-manifestation.md) | 145 | Glibc tcache poisoning & notebook page hook hijack |

</details>

<details>
<summary><b>Forensics & DFIR (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [Everything Left Open](POCTF%202026/forensics/everything-left-open.md) | 67 | Wireshark network stream reassembly & credential carving |
| Wave 2 | [A Cabin Worth](POCTF%202026/forensics/a-cabin-worth.md) | 119 | Deleted inode recovery from ext4 raw image |
| Wave 3 | [What Goes Unwritten](POCTF%202026/forensics/what-goes-unwritten.md) | 120 | Swap partition carving & volatile memory residue reconstruction |
| Wave 4 | [A Quiet Home](POCTF%202026/forensics/a-quiet-home.md) | 137 | Windows registry hive analysis & USB device history |
| Wave 5 | [Archaeology of Mistakes](POCTF%202026/forensics/archaeology-of-mistakes.md) | 100 | Corrupted tarball archive repair & gzip stream header reconstruction |
| Wave 6 | [The Apparatus, Ectograph](POCTF%202026/forensics/the-apparatus-ectograph.md) | 141 | Memory dump forensic extraction with Volatility 3 |
| Wave 7 | [Structural Failure](POCTF%202026/forensics/structural-failure.md) | 140 | SQLite transaction log forensic audit & deleted WAL pages |
| Wave 8 | [The Accused](POCTF%202026/forensics/the-accused.md) | 141 | Meridian Circle outbox analysis & syslog fragmentation triage |

</details>

<details>
<summary><b>Game Hacking (5 / 5)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 2 | [Leap of Faith](POCTF%202026/game%20hacking/leap-of-faith.md) | 87 | GH 1: Memory manipulation & gravity velocity patch |
| Wave 4 | [Health Is a Social Construct](POCTF%202026/game%20hacking/health-is-a-social-construct.md) | 138 | GH 2: 2D Shooter memory lock & invulnerability patch |
| Wave 5 | [The House Always Misses](POCTF%202026/game%20hacking/the-house-always-misses.md) | 100 | GH 3: Bullet-hell collision box removal & memory scanning |
| Wave 7 | [Terms and Conditions Apply](POCTF%202026/game%20hacking/terms-and-conditions-apply.md) | 141 | GH 4: Big boss fight damage multiplier injection |
| Wave 8 | [Client-Side Truth](POCTF%202026/game%20hacking/client-side-truth.md) | 141 | GH 5 (Final): 3D engine physics exploit & client state override |

</details>

<details>
<summary><b>Miscellaneous & Esoteric (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [The Apparatus, Invocation](POCTF%202026/misc/the-apparatus-invocation.md) | 101 | Morse audio demodulation & hidden spectral harmonics |
| Wave 2 | [Frequency and Consequence](POCTF%202026/misc/frequency-and-consequence.md) | 121 | DTMF tone sequence decoding & audio filtering |
| Wave 3 | [Columns of Holes](POCTF%202026/misc/columns-of-holes.md) | 127 | IBM 80-column punched card decoding |
| Wave 4 | [A Peculiar Game](POCTF%202026/misc/a-peculiar-game.md) | 137 | Conway's Game of Life cellular automaton backward state solve |
| Wave 5 | [Conditional Existence](POCTF%202026/misc/conditional-existence.md) | 162 | Prolog logic constraint satisfaction solver |
| Wave 6 | [The Tower of Babel](POCTF%202026/misc/the-tower-of-babel.md) | 141 | Polyglot code execution across 5 programming languages |
| Wave 7 | [Leave No Trace](POCTF%202026/misc/leave-no-trace.md) | 140 | Restricted Bash jail breakout & character whitelist bypass |
| Wave 8 | [The Ancient Instruction](POCTF%202026/misc/the-ancient-instruction.md) | 141 | Custom 8-instruction virtual machine emulator implementation |

</details>

<details>
<summary><b>Open-Source Intelligence (OSINT) (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [Where the Light Fails to Fall](POCTF%202026/osint/where-the-light-fails-to-fall.md) | 123 | Shadow angle analysis, solar ephemeris, and architectural geolocation |
| Wave 2 | [A Borrowed Name](POCTF%202026/osint/a-borrowed-name.md) | 102 | Historical maritime registry & archive record tracing |
| Wave 3 | [Strings Attached](POCTF%202026/osint/strings-attached.md) | 102 | Git commit history analysis, deleted branches, and author identity mapping |
| Wave 4 | [The Apparatus, Apport](POCTF%202026/osint/the-apparatus-apport.md) | 137 | Waymarking & historical patent search |
| Wave 5 | [The Preserved Moment](POCTF%202026/osint/the-preserved-moment.md) | 100 | Street View temporal comparison & intersection triangulation |
| Wave 6 | [What Was Exposed](POCTF%202026/osint/what-was-exposed.md) | 141 | Public S3 bucket misconfiguration & historical cache scraping |
| Wave 7 | [The View from Above](POCTF%202026/osint/the-view-from-above.md) | 140 | Flight radar ADS-B telemetry correlation |
| Wave 8 | [Following the Money](POCTF%202026/osint/following-the-money.md) | 100 | Reconstructed $1 bill serial tracking & EXIF metadata triangulation |

</details>

<details>
<summary><b>Reverse Engineering (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [Excavation](POCTF%202026/reverse%20engineering/excavation.md) | 122 | Stripped x86_64 ELF disassembly & control-flow flattening deobfuscation |
| Wave 2 | [The Disassembled Mind](POCTF%202026/reverse%20engineering/the-disassembled-mind.md) | 118 | State machine decompilation & anti-debugging detection defeat |
| Wave 3 | [Panoptican](POCTF%202026/reverse%20engineering/panoptican.md) | 112 | Windows PE x64 binary patching & license check bypass |
| Wave 4 | [An Invented Language](POCTF%202026/reverse%20engineering/an-invented-language.md) | 132 | Custom virtual machine architecture disassembler |
| Wave 5 | [The Oracle's Weight](POCTF%202026/reverse%20engineering/the-oracle-s-weight.md) | 140 | Neural network model weights extraction & decision boundary inversion |
| Wave 6 | [The Oxidized Archive](POCTF%202026/reverse%20engineering/the-oxidized-archive.md) | 145 | Rust binary reverse engineering & iterator chain analysis |
| Wave 7 | [The Apparatus, Dissolution](POCTF%202026/reverse%20engineering/the-apparatus-dissolution.md) | 140 | Z3 SMT constraint solving for complex mathematical key check |
| Wave 8 | [Against the Clock](POCTF%202026/reverse%20engineering/against-the-clock.md) | 145 | Time-locked KDF reversal, epoch reconstruction, & dynamic hooking |

</details>

<details>
<summary><b>Steganography (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [Invisible Ink](POCTF%202026/steganography/invisible-ink.md) | 113 | Zero-width Unicode character extraction and binary conversion |
| Wave 2 | [Commit to Memory](POCTF%202026/steganography/commit-to-memory.md) | 128 | Git packfile commit object metadata injection |
| Wave 3 | [The Apparatus, The Rapping](POCTF%202026/steganography/the-apparatus-the-rapping.md) | 120 | Audio spectral analysis & Morse code watermark discovery |
| Wave 4 | [Velocity](POCTF%202026/steganography/velocity.md) | 137 | Frame-rate timing anomaly & video packet delay encoding |
| Wave 5 | [The Hidden Path](POCTF%202026/steganography/the-hidden-path.md) | 100 | LSB image steganography across RGB bit planes |
| Wave 6 | [The Wrong Channel](POCTF%202026/steganography/the-wrong-channel.md) | 141 | Alpha channel manipulation & PNG ancillary chunk forensic inspection |
| Wave 7 | [The Geometry of Secrets](POCTF%202026/steganography/the-geometry-of-secrets.md) | 140 | 3D OBJ model vertex coordinate manipulation extraction |
| Wave 8 | [The Pattern Language](POCTF%202026/steganography/the-pattern-language.md) | 100 | Plaid tartan sett thread sequence decoding & RGB thread pitch analysis |

</details>

<details>
<summary><b>Web Exploitation (8 / 8)</b></summary>
<br>

| Wave | Challenge | Points | Focus / Technique |
| :---: | :--- | :---: | :--- |
| Wave 1 | [The Shape of a Query](POCTF%202026/web/the-shape-of-a-query.md) | 97 | Blind Boolean-based SQL injection with automated binary search |
| Wave 2 | [Poisoned Well](POCTF%202026/web/poisoned-well.md) | 95 | DOM-based XSS via unsanitized URL hash fragment |
| Wave 3 | [No Structure Required](POCTF%202026/web/no-structure-required.md) | 109 | NoSQL injection bypass on MongoDB authentication query |
| Wave 4 | [The Logic Inside](POCTF%202026/web/the-logic-inside.md) | 137 | Server-Side Template Injection (SSTI) in Jinja2 to RCE |
| Wave 5 | [The Apparatus, Levitation](POCTF%202026/web/the-apparatus-levitation.md) | 100 | WebSocket protocol manipulation & state hijacking |
| Wave 6 | [The Interior Route](POCTF%202026/web/the-interior-route.md) | 141 | Server-Side Request Forgery (SSRF) bypassing local metadata filters |
| Wave 7 | [Between the Lines](POCTF%202026/web/between-the-lines.md) | 139 | HTTP Request Smuggling (CL.TE desync) |
| Wave 8 | [The State of Trust](POCTF%202026/web/the-state-of-trust.md) | 141 | OAuth 2.0 PKCE downgrade & auditor trust-seal bypass |

</details>

---

## Tooling & Methodology

The solutions documented across this repository leverage offensive security frameworks and standard analysis tooling:

- **Binary Exploitation & Reversing**: `pwntools`, `GDB / GEF`, `Ghidra`, `IDA Pro`, `angr`, `Z3 Theorem Prover`, `faketime`
- **Forensics & Incident Response**: `Volatility 3`, `Wireshark / tshark`, `binwalk`, `scalpel`, `foremost`, `exiftool`
- **Web & Cryptography**: `Burp Suite Professional`, `Caido`, `Python (cryptography, gmpy2, sympy)`, `sqlmap`
- **OSINT & Reconnaissance**: SunCalc ephemeris, Google Earth historical imagery, FAA ADS-B registries, EXIF triangulation

---

<p align="center">
  <i>Crafted with precision by <b>iblamedev</b> for Pointer Overflow CTF 2026.</i><br>
  <i>“Become so untouchable that even the universe regrets teaching you how to suffer.”</i>
</p>
