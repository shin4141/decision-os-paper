# Adoption (GitHub Actions) — SiriusA Policy Pack (V5)

This page shows the minimal adoption path.
This repo is **spec-only**. Canonical engine & schemas live in `mmar-l0-core`.

- Engine: https://github.com/shin4141/mmar-l0-core
- Schemas:
  - decision_gate: https://github.com/shin4141/mmar-l0-core/blob/main/schema/decision_gate.schema.json
  - mmar_findings: https://github.com/shin4141/mmar-l0-core/blob/main/schema/mmar_findings.schema.json

## Minimal workflow (copy-paste)

Create a workflow file in your repo:

- `.github/workflows/siriusa-gate.yml`

```yaml
name: SiriusA Gate (V5 policy pack)

on:
  workflow_dispatch:

jobs:
  gate:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      # NOTE: This is a spec repo. Replace the next step with the actual engine call.
      # The canonical reference implementation lives in `mmar-l0-core`.
      - name: Run gate (reference)
        run: |
          echo "This is a spec-only template."
          echo "Run the canonical engine from: https://github.com/shin4141/mmar-l0-core"
          exit 1

      - name: Upload decision artifacts
        if: always()
        uses: actions/upload-artifact@v4
        with:
          name: siriusa-gate
          path: |
            decision_gate.json
            mmar_findings.json
　```
