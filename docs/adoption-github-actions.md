# Adoption (GitHub Actions) — SiriusA Policy Pack (V5)

This page contains a **spec-only adoption template**. It intentionally exits with failure until an adopter supplies the actual engine invocation. This repository also has a separate working [synthetic demo](../README.md#decision-gate-demo-actions); the template below is not that demo.
Canonical engine & schemas live in `mmar-l0-core`:
- Engine: https://github.com/shin4141/mmar-l0-core
- decision_gate schema: https://github.com/shin4141/mmar-l0-core/blob/main/decision_gate.schema.json
- mmar_findings schema: https://github.com/shin4141/mmar-l0-core/blob/main/mmar_findings.schema.json

## Minimal workflow (copy-paste)

Create this file in your repo:
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

      # NOTE: Spec-only template. Replace this step with the canonical engine call.
      - name: Run gate (reference)
        run: |
          echo "Spec-only template."
          echo "Use canonical engine: https://github.com/shin4141/mmar-l0-core"
          exit 1

      - name: Upload decision artifacts (optional)
        if: always()
        uses: actions/upload-artifact@v4
        with:
          name: siriusa-gate
          path: |
            decision_gate.json
            mmar_findings.json
```
