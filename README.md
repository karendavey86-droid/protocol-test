[![Created with Ule Lab Protocol Template](https://img.shields.io/badge/created%20with-Ule%20Lab%20Protocol%20Template-blue)](https://github.com/ulelab/protocol-template)
[![Template version](https://img.shields.io/github/v/release/ulelab/protocol-template)](https://github.com/ulelab/protocol-template/releases)

# 3’end RNA-seq using template switching protocol

### Status: 🟡 `[?]` | partially migrated / unconfirmed
| ***Status legend***: | 🟢 `[OK]` working | 🟡 `[?]` unconfirmed / partial | 🔴 `[X]` broken |
|---|---|---|---|

# About

Protocol for 3’ end RNA-seq using a template switching reverse transcription workflow.

## Contents
1. [RNA extraction](#1-rna-extraction)
2. [RNA fragmentation and template switching RT](#2-rna-fragmentation-and-template-switching-rt)
3. [Template switching RT incubation and cleanup](#3-template-switching-rt-incubation-and-cleanup)
4. [Optional PCR test](#4-optional-pcr-test)
5. [Indexing PCR](#5-indexing-pcr)
6. [PCR beads purification](#6-pcr-beads-purification)
7. [Buffers](#7-buffers)
8. [Migration notes](#migration-notes)

---

# 1. RNA extraction

**Input / starting material:** RNA lysate

- Maxwell RNA extraction
- Alternative: Add 3 volumes of LS-Trizol to lysate
- Extract RNA using the Zymo MicroSpin Columns
- Elute with 6 µL of H₂O

---

# 2. RNA fragmentation and template switching RT

- Prepare fragmentation buffer.
- Fragmentation buffer: 80 mM Tris-HCl pH 7.5, 40 mM MgCl₂.
> **Note**: have more recently been using milder fragmentation buffer conditions with input concentration of 10 mM Tris-HCl pH 7.5, 5 mM MgCl₂ (final concentration 1.25 mM Tris-HCl and 0.625 mM MgCl₂).
- Use 500 ng of RNA (whenever possible).
- Bring to 3.5 µL using water.
- Add 0.5 µL of fragmentation buffer (10 mM Tris-HCl pH 7.5, 5 mM MgCl₂ final concentration).
- Fragment RNA by incubating 12 min at 95 °C.
- Add:
  - 0.5 µL 10 mM dNTPs
  - 0.5 µL 5 µM primer RT1
- Mix and incubate at 65 °C for 3 min then cool down to 42 °C and hold.

---

# 3. Template switching RT incubation and cleanup

- Make a mastermix and add 5.5 µL of the following:
  - 2 µL of SSIV buffer
  - 2 µL 5 M betaine
  - 0.5 µL 0.1 M DTT
  - 0.25 µL 40 µM TSO
  - 0.25 µL 200 mM MgCl₂
  - 0.25 µL SuperRNasin
  - 0.25 µL SSIV
- Place the mastermix into a PCR strip and into the cycler so that it pre-warms to 42 °C before you start adding it to the samples.
- Add mastermix to samples while keeping them at 42 °C in the cycler (i.e., don’t take the samples out of the cycles while adding the mix).
- Incubate at 42 °C for 10 min.
- Incubate at 50 °C for 30 min.
- Purify using Magbind beads (1.8 µL per 1 µL of PCR reaction). Elute in 8 µL H₂O.

---

# 4. Optional PCR test

- Use 1 µL RT product.

---

# 5. Indexing PCR

- Prepare the following 20 µL indexing PCR reaction for each sample:
  - 10 µL of 2× Q5
  - 2 µL RT product
  - 1 µL dual indexed primers
    - Use a different index for each sample.
    - Make sure each sample will have a different index if submitting multiple libraries at the same time.
  - 7 µL of ddH2O
- Incubate for the PCR reaction using the Q5 program:
  - Extension time – 45 seconds
  - Tm – 65 °C
  - Typically try 10 and 14 cycles
- Move samples to post-PCR room.
- Add 2 µL of purple 6X loading buffer to 5 µL of PCR reaction. Keep the rest of the 20 µL.
- Load on a 6% TBE gel together with 2 µL of ready-to-use low molecular weight ladder (NEB).
- Run at 180 V for 25 min.
- Stain with Sybr Green (1:10000 dilution) in 1X TBE.
- Visualise.

---

# 6. PCR beads purification

- Mix together approx. 10 µL of each PCR reaction.
- Add a suitable amount of Magbind beads (e.g. 0.9 µL per 1 µL of PCR reaction) and mix.
- Incubate at room temperature for 5 minutes.
- Remove supernatant and wash with 500 µL of 70% Ethanol for 30 sec. Repeat this step.
- Air dry the beads.
- Resuspend in 30 µL of H₂O.

---

# 7. Buffers

- Fragmentation buffer: 80 mM Tris-HCl pH 7.5, 40 mM MgCl₂.
- Milder fragmentation buffer conditions: input concentration of 10 mM Tris-HCl pH 7.5, 5 mM MgCl₂ (final concentration 1.25 mM Tris-HCl and 0.625 mM MgCl₂).

---

# Migration notes

- Source files: legacy/source.txt, legacy/source.pdf
- Migration date: 2026-04-13
- Imported protocol metadata from source-metadata.yml:
  - source_type: pdf
- Template metadata from docs/template-metadata.yml:
  - template_repository: ulelab/protocol-template
  - template_url: https://github.com/ulelab/protocol-template
  - template_license: GPL-3.0
  - template_authors:
    - name: Ule lab
    - name: Ira A. Iosub
  - template_version: 1.0.0dev
  - template_release_date: 2026-04-10
- Formatting normalizations performed:
  - added spaces between numbers and units
  - standardized `µL`, `°C`, `H₂O`, `min`, and `sec`
  - standardized `1X TBE` and `6X loading buffer`
- Ambiguities and uncertainty flagged:
  - No content required guessing; original protocol text was preserved.

## Unplaced content

None.
