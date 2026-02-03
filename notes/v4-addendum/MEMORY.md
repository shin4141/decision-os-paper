# MEMORY — Decision-OS V4 Addendum
As-of: 2026-02-03
Scope: High-stakes / irreversible decisions
Goal: Convert grounded evaluation into a reproducible gate: GO / HOLD / NO

---

## 1) Canonical output (required)
Gate ∈ {GO, HOLD, NO}

- GO   : allowed to proceed now
- HOLD : not allowed to proceed (must fill missing evidence first)
- NO   : not allowed to proceed (reject or redesign)

---

## 2) Inputs (provided by the user)
- Decision (1 line): what action will be taken
- Deadline: by when
- Reversibility: reversible / partially / irreversible
- Rate (JPY/hour)
- Time saved (hours, estimate)
- Maintenance time (hours: initial + ongoing)
- Gross profit (per conversion)
- Volume (expected count in the period)
- CVR (pessimistic / base / optimistic) — 3 scenarios
- Thresholds: h_mid, h_ev (optional; can be blank)

---

## 3) Computation (output by AI)
Formula:
(time_saved_h × rate × 4) + (CVR × gross_profit × volume) − (maintenance_h × rate × 4)
→ Practical gain (pess/base/opt)= __ / __ / __

EV:
pess=__  base=__  opt=__
Expected EV (0.2/0.6/0.2)= __

---

## 4) Decision rule (output by AI)
IF practical_gain(base) ≥ h_mid AND expected_EV ≥ h_ev THEN GO
ELSE HOLD/NO (1-line reason)

HOLD must follow this rule:
- HOLD is not “maybe”; it is “not allowed yet”.
- When HOLD, list missing evidence in verifiable form (URLs, screenshots, confirmations, tests, etc.).

---

## 5) Premortem (output by AI)
Provide 3 sets: cause / signal / avoidance (max 3 lines × 3)

---

## 6) Fixed output format (AI must follow)
1) Practical gain (pess/base/opt)
2) EV (pess/base/opt) + Expected EV
3) Gate (GO/HOLD/NO) + 1-line reason
4) If HOLD: missing evidence list
5) Premortem × 3
6) Next action (only one)

---

## 7) Disclosure boundary
Public:
- I/O, formula, decision rule, HOLD discipline, output format
Not disclosed:
- private calibration values, sensitive heuristics, personal rationale for thresholds

---

## 8) Files in this folder
- README.md (human entry point)
- Main PDF (V4 Addendum)
- MEMORY.md (this file, canonical EN)
- MEMORY_JA.md (Japanese)
