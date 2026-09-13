# Decision-OS V13 Research Notes

V13 studies **Compound Loop Governance**: whether another AI-assisted iteration should run, wait, be capped, or stop, so that repetition improves the conditions for future work without damaging its Carrier (the people, resources, and recovery capacity needed to continue).

## Published notes

- **Start with v0.2:** [Post-Optimization Survival Architecture — Compound Loop Governance for AI Operations](https://doi.org/10.5281/zenodo.20634743), working paper, 2026-06-11; [local PDF](Decision-OS_V13_Research_Note_v0.2.pdf).
- **Earlier v0.1:** [Compound Loop — Selecting the Variable That Makes the Next Iteration 1.01](https://doi.org/10.5281/zenodo.20604577), working paper, 2026-06-09; [local PDF](Decision-OS_V13_Research_Note_v0.1.pdf).

V0.2 remains a **Research Note / Canon Freeze / Prototype-Bound Draft**, even though it is publicly deposited. Its `IsNewVersionOf` relation points to v0.1; both belong to concept DOI `10.5281/zenodo.20604576`. A final v1.0 paper was not verified. The original “v1.0 after prototype feedback” direction is a plan, not a publication claim.

## Public implementation and results

[V13 LoopKit](https://github.com/shin4141/decision-os-v13-loopkit) is a separate operating prototype. Its current entry describes next-loop reporting, restartable handoffs, selective external-memory reuse, and a bounded local scanner. Start with the [English onboarding guide](https://github.com/shin4141/decision-os-v13-loopkit/blob/main/docs/external_intelligence_onboarding.md); no full-corpus read is needed.

Use the gateway's [implementation and evidence table](../../README.md#public-implementations-and-evidence) for fixed-commit results: Forward Use 003/004, a three-repository scanner trial, local onboarding tests, and the Cycle 006 failure boundary. These include creator-owned observations, limited usefulness, and unestablished whole-flow behavior. They are not proof of the full V13 theory, independent certification, or model self-training.

[Software v0.1.0](https://github.com/shin4141/decision-os-v13-loopkit/releases/tag/v0.1.0) is the first operating prototype snapshot. Software main has evolved since that release; do not confuse it with research-note v0.1 or v0.2.

## V12 → V13

```text
V12 Completion Record: is the work restartable enough to close?
        ↓
V13 Loop Record: should the next cycle GO / HOLD / CAP / BLOCK?
        ↓
A bounded next action with explicit conditions
```

V12 addresses false completion; V13 addresses unjustified or non-compounding repetition. The note's central canon is “Capability without controllability is not intelligence.” It is a research position, not evidence that all proposed mechanisms have been implemented.

Continue to [V14](../v14/README.md) for burden and ownership across handoffs, or return to the [series index](../../README.md#series-index-zenodo).
