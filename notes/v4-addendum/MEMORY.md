# MEMORY — Decision-OS V4 Addendum
As-of: 2026-02-03
Scope: Grounded Decision Protocol (V5-compatible Guard)

## 1) Purpose (Why)
Prevent irreversible mistakes in high-stakes actions by forcing a grounded, checkable workflow.

## 2) What it is (What)
A decision protocol that outputs one of:
- GO
- HOLD
- NO

## 3) Core primitives (Definitions)
- As-of: evaluate with information/constraints available at the time.
- Scenario set: best / base / worst (minimum 3).
- Evidence: what must be true to move HOLD→GO.

## 4) Input → Output (Interface)
Input:
- decision statement
- constraints
- scenario set (3+)
- evidence list (current + missing)

Output:
- gate ∈ {GO, HOLD, NO}
- reason (1–3 bullets)
- missing_evidence (only if HOLD)
- next_action (single step)

## 5) Disclosure boundary
Public: reproducible workflow + interface + examples.
Not disclosed: private calibration / personal thresholds / sensitive heuristics.

## 6) Files
- Main PDF: Decision_OS_V4_Addendum_...Guard.pdf
- README: entry point
