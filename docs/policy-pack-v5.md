# SiriusA Policy Pack (V5) — Minimal Spec

This repo documents the V5 (SiriusA) policy pack semantics.
Canonical execution/engine lives elsewhere; this repo fixes the *meaning* and *usage*.

## Severity
- PASS: safe to proceed
- DELAY: not safe to decide now (time-gated recheck; e.g., +48h)
- BLOCK: do not proceed

## Core boundary (V5)
The policy pack focuses on life-protection & irreversible-risk prevention:
- wallet signing / approvals
- fraud / social engineering patterns
- high externality × high irreversibility actions

## Outputs (contract)
The gate emits a machine-readable decision:
- `severity` (PASS|DELAY|BLOCK)
- `reason_codes` (stable identifiers)
- `suggested_fix` (what to change)
- `recheck` (when/what to re-evaluate)

Schemas are canonical in `mmar-l0-core`:
- decision_gate schema: https://github.com/shin4141/mmar-l0-core/blob/main/schema/decision_gate.schema.json
- mmar_findings schema: https://github.com/shin4141/mmar-l0-core/blob/main/schema/mmar_findings.schema.json

## Adoption (GitHub Actions)
See: `docs/adoption-github-actions.md` 
