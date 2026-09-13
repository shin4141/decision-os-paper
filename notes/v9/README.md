# Decision-OS V9.1 — Impact-Weighted Release

This folder preserves the V9 / V9.1 manuscripts. Publication is not a claim of peer review or empirical validation of the release protocol. See the [series index](../../README.md#series-index-zenodo) and [implementation evidence](../../README.md#public-implementations-and-evidence).

## Current reading edition

**Decision-OS V9.1: Impact-Weighted Release**  
*From Continuous-Pass Gates to Condition-Bound Judgment Reuse*

V9.1 extends V9 from an impact-weighted release protocol into a reusable judgment-state protocol.  
The main additions are:

- Judgment Compression
- Residue Criterion
- condition-bound judgment reuse
- condition invalidation → DELAY
- reusable gate states: `(outcome, residue_key, condition)`

## Published editions

- **V9.1:** [DOI 19935535](https://doi.org/10.5281/zenodo.19935535), published preprint, 2026-05-01; deposited version `v9.1`. The record explicitly declares `IsNewVersionOf` the v2 record below.
- **v2 (Jan 27, 2026):** https://doi.org/10.5281/zenodo.18390432
- **v1 (Jan 21, 2026):** https://doi.org/10.5281/zenodo.18321009

## Files

### Paper (PDF)

- [V9.1 PDF](Decision__O_S_V9__1_1.pdf) — Decision-OS V9.1: Impact-Weighted Release
- [V9 Japanese PDF](Decision-OS_V9_Impact-Weighted_Release_v1_JP.pdf), deposited `v1`.
- [V9 English PDF](Decision-OS_V9_Impact-Weighted_Release_v1_EN.pdf), deposited `v2`; the local filename retains `v1`.

### Historical figure references

The earlier guide listed `fig/fig1_judgment_compression_pipeline.png`, `fig/fig2_release_gate_structure.png`, and three V9 legacy images under `fig/`. Those paths are absent from this checkout; use the figures embedded in the paper PDFs. No files were moved or recreated.

## V9.1 summary

V9 fixed the three anchors:

1. **As-of** — temporal fidelity
2. **Seat** — responsibility and decision rights
3. **Release** — impact-weighted continuous pass

V9.1 preserves these anchors and adds a reuse layer:

DFR → Residue Criterion → Judgment Compression → Condition-Bound Reuse

A compressed judgment is stored as:

(outcome, residue_key, condition)

If the stored condition becomes invalidated, stale, or unverified, the judgment does not remain PASS by default.
It is downshifted to DELAY and must be rechecked through DFR.

Quick verification

Use the version DOI for citation. The old lock metadata below is preserved for historical inspection; it does not establish byte identity with the current V9.1 deposit. Direct Zenodo file comparison was not completed in this audit.

Notes
Figures are labeled in English for reuse across JP/EN versions.
Canon notation is unified: evidence = UNION.
V9.1 treats probability-related variables such as p or P as auxiliary inputs, not the main object of the protocol.
The main object of V9.1 is the reusable judgment state that survives As-of review, DFR, residue filtering, and Judgment Compression.
Lock commit
V9 legacy lock commit (EN): 1613b8f80a598ccb7fff3e67209214bf0fd402d4
V9.1 lock commit: to be added
