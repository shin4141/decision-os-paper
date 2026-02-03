# MEMORY — Decision-OS V4 Addendum (Grounded Decision Protocol)
As-of: 2026-02-03
Role: machine-readable memory card
Scope: high-stakes, irreversible actions (V5-compatible Guard)

## 0) Canonical output
Gate ∈ {GO, HOLD, NO}
- GO   : proceed now
- HOLD : do not proceed; gather missing evidence
- NO   : do not proceed; reject or redesign the decision

## 1) Minimal interface (I/O)
### Input (required)
- decision: one-sentence action (what will be done)
- constraints: hard limits (time, money, safety, legality, commitments)
- reversibility: reversible / partially / irreversible
- scenarios: at least 3 {best, base, worst}
- evidence_current: what is already verified
- evidence_missing: what must be verified before GO

### Output (required)
- gate: GO | HOLD | NO
- reason: 1–3 bullets (why)
- missing_evidence: list (only when HOLD)
- next_action: single step (only one)

## 2) Grounded protocol (steps)
1. Write decision + constraints + reversibility (As-of).
2. Produce scenarios (best/base/worst) with concrete outcomes.
3. Identify evidence: what must be true for GO.
4. Decide:
   - If any critical evidence is missing → HOLD
   - If constraints are violated or worst-case unacceptable → NO
   - If evidence sufficient and constraints satisfied → GO

## 3) Evidence rule (how HOLD works)
- HOLD is not “maybe”; it is “not allowed yet”.
- HOLD must list missing evidence in checkable form (URLs, screenshots, docs, confirmations, tests).

## 4) Disclosure boundary
Public:
- interface (I/O), step protocol, examples, reproducible workflow
Not disclosed:
- private calibration, personal thresholds, sensitive heuristics

## 5) Files in this folder
- README.md (human entry point)
- Decision_OS_V4_Addendum_Grounded_Decision_Protocol_V5_Compatible_Guard.pdf (main)
- MEMORY.md (this file)

