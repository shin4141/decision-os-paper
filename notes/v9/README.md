# Decision-OS V9.1 — Impact-Weighted Release

This folder contains the finalized paper PDF(s) and locked figures for Decision-OS V9 / V9.1.

## Latest version

**Decision-OS V9.1: Impact-Weighted Release**  
*From Continuous-Pass Gates to Condition-Bound Judgment Reuse*

V9.1 extends V9 from an impact-weighted release protocol into a reusable judgment-state protocol.  
The main additions are:

- Judgment Compression
- Residue Criterion
- condition-bound judgment reuse
- condition invalidation → DELAY
- reusable gate states: `(outcome, residue_key, condition)`

## Latest DOI (recommended)

- **V9.1:** DOI pending / to be added after Zenodo release
- **v2 (Jan 27, 2026):** https://doi.org/10.5281/zenodo.18390432
- **v1 (Jan 21, 2026):** https://doi.org/10.5281/zenodo.18321009

## Files

### Paper (PDF)

- `Decision__O_S_V9__1_1.pdf` — Decision-OS V9.1: Impact-Weighted Release
- `Decision-OS_V9_Impact-Weighted_Release_v1_JP.pdf`
- `Decision-OS_V9_Impact-Weighted_Release_v1_EN.pdf`

### Figures (V9.1 final, locked)

- `fig/fig1_judgment_compression_pipeline.png` — Judgment Compression Pipeline under As-of review
- `fig/fig2_release_gate_structure.png` — Release Gate Structure under Impact-Weighted Observation

### Figures (V9 legacy)

- `fig/Fig1_final_v9_v8_to_v9..jpg` — V8→V9 connection
- `fig/Fig2_final_public_tube_union.jpg` — Public Tube `(p,n)`: cumulative risk and defense levers
- `fig/Fig3_final_release_volume.jpg` — Impact-Weighted Release Volume

## V9.1 summary

V9 fixed the three anchors:

1. **As-of** — temporal fidelity
2. **Seat** — responsibility and decision rights
3. **Release** — impact-weighted continuous pass

V9.1 preserves these anchors and adds a reuse layer:

```text
DFR → Residue Criterion → Judgment Compression → Condition-Bound Reuse

A compressed judgment is stored as:

(outcome, residue_key, condition)

If the stored condition becomes invalidated, stale, or unverified, the judgment does not remain PASS by default.
It is downshifted to DELAY and must be rechecked through DFR.

Quick verification

Open this folder at the lock commit below and compare the PDF + figures with the Zenodo record.

Notes
Figures are labeled in English for reuse across JP/EN versions.
Canon notation is unified: evidence = UNION.
V9.1 treats probability-related variables such as p or P as auxiliary inputs, not the main object of the protocol.
The main object of V9.1 is the reusable judgment state that survives As-of review, DFR, residue filtering, and Judgment Compression.
Lock commit
V9 legacy lock commit (EN): 1613b8f80a598ccb7fff3e67209214bf0fd402d4
V9.1 lock commit: to be added
