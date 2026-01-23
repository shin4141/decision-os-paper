![Decision Gate](https://github.com/shin4141/decision-os-paper/actions/workflows/decision-gate.yml/badge.svg)

**Decision Gate demo (Actions):** Run workflow → `scenario=pass` (green) / `scenario=block` (red).  
Generates `decision_gate.json` via `mmar-l0-core` and enforces PASS/DELAY/BLOCK in CI.
Output includes `reason_codes`, `evidence_paths`, and `suggested_fix` in `decision_gate.json` (Artifacts).

**Crypto example** (wallet signing / approvals): If a signing/approval request (Approve/Permit) has no evidence (e.g., screenshot/log/target URL/revoke note), the gate returns DELAY. If it is high externality × high irreversibility with no evidence, it returns BLOCK. Check decision_gate.json in GitHub Actions Artifacts.

## Quick demo
1) Actions → Decision Gate (B-min penetration) → Run workflow  
2) scenario=pass → green / scenario=delay → yellow / scenario=block → red
3) Download artifact: run page → Artifacts → `decision_gate` (contains `decision_gate.json`)

# Decision-OS Paper (V4–V9)

This repository is the **public gateway** for the Decision-OS series.  
Canonical artifacts are hosted on **Zenodo (DOI)**; GitHub is used for **indexing and evidence routing**.

---

## Start here (Gateway)

Decision-OS has **two entry paths**. Pick the one that matches your interest.

**Citation:** Citation (quick)
- Implementation: cite V5 (SiriusA)
- Adoption gate entry: cite V5 Addendum (0.3)
- Control/gateway framing: cite V8 v2 (Time-Tube)
- Implementation (MMAR / L0 core): https://github.com/shin4141/mmar-l0-core
 (CI + schema contract)


### A) Practical Safety / Implementation (Real-world)
Quick entry (3 short addenda, links only)
- V5 Addendum (0.3) — SiriusA Adoption Gate (state machine + HOLD(evidence) + five-line contract)
  https://doi.org/10.5281/zenodo.18252623
- V6 Addendum (1p) — Verification Note for PIC (evaluation hooks; falsifiable protocol)
  https://doi.org/10.5281/zenodo.18240015
- V7 Addendum (0.3) — Why Aspire and Why PIC (minimal necessity)
  https://doi.org/10.5281/zenodo.18220351

(If you only read one: start with V5 Addendum.)

**Start with V5** — ZK-backed approval, two-step confirmation, revoke window (Δt), duress-aware control.  
- V5 — SiriusA: Zero-Knowledge Confirmation Layer for the Protection of Life  
  https://zenodo.org/records/18051625

**Then**: V6 → V8 (conceptual expansion)

### B) AGI Theory / Control (Series overview)
**Start with V8 (v2)** — series gateway framing (Time-as-an-Ally, control structure).  
- V8 (v2) — Time-Tube Control for Self-Safe AGI  
  https://zenodo.org/records/18137204  
  Concept DOI (all versions): 10.5281/zenodo.17970577  
  SSOT SHA (V8): a771021949fabf4b0ea23141863bab5f1a266e8c

**Then**: V6 (PIC) → V7 → (back to V5 for implementation details)

---

## Series Index (Zenodo)

- **V4** — Polaris-Origin: An Entry OS for Seeing Structure with AI  
  https://doi.org/10.5281/zenodo.17905930

- **V5** — SiriusA: Zero-Knowledge Confirmation Layer for the Protection of Life  
  https://doi.org/10.5281/zenodo.18051625

- **V5 Addendum (0.3)** — SiriusA Adoption Gate: Hold-First Auditing for Irreversible Actions (Supplement; adoption fit check, state machine, evidence bundle)  
  https://doi.org/10.5281/zenodo.18252623

- **V6** — (PIC) Canonical Memory Architecture for Self-Recursive Intelligence  
  https://doi.org/10.5281/zenodo.17717518

- **V6 Addendum (Verification Note, 1p)** — Evaluation Hooks for PIC (Supplement; evaluation hooks, protocol, falsify)  
  https://doi.org/10.5281/zenodo.18240015

- **V7** — Aspire Intelligence for AGI: An Operational and Self-Recursive Structural Definition of AGI (A×G×I)  
  https://doi.org/10.5281/zenodo.17932554

- **V7 Addendum (0.3)** — Why Aspire and Why PIC (Supplement; minimal necessity of Aspire and PIC)  
  https://doi.org/10.5281/zenodo.18220351

- **V8 (v2)** — Time-Tube Control for Self-Safe AGI  
  https://doi.org/10.5281/zenodo.18137204  
  Concept DOI (all versions): https://doi.org/10.5281/zenodo.17970577  
  SSOT SHA (V8): a771021949fabf4b0ea23141863bab5f1a266e8c

- **V9 (v1, JP)** — Impact-Weighted Release (Japanese Edition)<br>
  https://doi.org/10.5281/zenodo.18321009<br>
  Concept DOI (all versions): https://doi.org/10.5281/zenodo.18321008


---

## Notes (Zenodo)

**Time-is-an-Ally v2** — Value amplification with disciplined re-evaluation (Ta) and discoverability (Da)  
- **Zenodo (v2, version DOI):** https://doi.org/10.5281/zenodo.18211673  
- **Zenodo (v1, 1P minimal):** https://doi.org/10.5281/zenodo.18158755  
- **Source (GitHub):** notes/time-is-an-ally/

---

## How to read (60 seconds)

If a model is fluent, do not trust the summary. Start from claims:

**Claims → Assumptions → Dependencies → CheckType → Falsifier → then summarize.**

---

## Companion Tool (Unlisted)
⚖️ Decision Insurance — personal decision structuring (not legal/tax/medical/investment advice).  
Fixed order: max loss → 3 failure modes → hedge → verdict + one next step.  
▶︎ - Tools hub: https://github.com/shin4141/decision-os-paper/blob/main/notes/tools.md

---

## Repository structure (quick)

- `assets/` — public figures and media
- `evidence/` — evidence ZIP / stamps / proof of work (dated folders)
- `notes/` — short notes and supplements
- `AUTHORS_NOTE.md` — transparency/disclosure note
- `CITATION.cff` — citation metadata

---

## Citation

Use **Zenodo DOIs** as the canonical citation targets (preferred).  
GitHub is the gateway and evidence router.

## Links
- X: https://x.com/DecisionOS
- - Transparency (Author’s Note): [AUTHORS_NOTE.md](./AUTHORS_NOTE.md)
  
正典=ProjectFiles(v2025-11-03) / DOI:10.5281/zenodo.17511725 / SHA256=0941d922...

DOI: 10.5281/zenodo.17480645 ｜ SSOT: 840c85de344f5dd197dc5122ad9f4ba452f2970d
(this PDF matches this commit)

Author: **Shinichi Nagata** — Independent Researcher, Kanagawa, Japan  
Contact: **siriusa.paper@gmail.com**

SSOT: GitHub (decision-os-paper). This PDF keeps only constants & skeleton; canonical text is the repo.

**Evidence (2025-11-04, Chigasaki JP Post):** [evidence/2025-11-04](https://github.com/shin4141/decision-os-paper/tree/main/evidence/2025-11-04) — commit [`991d81e2a7`](https://github.com/shin4141/decision-os-paper/commit/991d81e2a7531ae6ab565ce2ced77ed2605fda6f)

# decision-os-paper
