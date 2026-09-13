# Decision-OS research gateway

Decision-OS studies how human–AI work can remain controllable over time: how to make decisions, integrate updates, preserve usable memory, close work so it can be resumed, and decide whether another cycle or public release is justified. It proposes structures for keeping evidence, responsibility, stop conditions, and recovery paths attached to decisions.

**Current orientation (2026-09-13):** this gateway covers **V4–V14**, including V10 goal rescaling, V11 reconnectable memory, V12 completion integrity, V13 loop governance, and the V14 Resource Justice research note. V14 is the newest research note listed here; it does not replace the earlier layers. Public V12 software and the evolving V13 LoopKit prototype have separate [implementation and validation paths](#public-implementations-and-evidence).

These are published research artifacts, mostly preprints or working papers, plus bounded software prototypes. **Public availability does not establish peer review, empirical validation of the whole theory, or a general performance guarantee.** No peer-review outcome was verified in this audit. DOI metadata was checked against Zenodo's records registered with DataCite; direct Zenodo page/download access timed out. See the [source and verification record](docs/gateway_update_2026-09-13.md) for exact limits.

## Start here (Gateway)

You do not need to read every volume. Pick the problem closest to your work; follow the optional background only when needed.

| Interest | Start with | Continue if useful |
| --- | --- | --- |
| Memory and reconnection across AI sessions | [V11: Forget for Future](notes/v11/README.md) — compress context while keeping a path to evidence and stop conditions | [V12](notes/v12/README.md) for closure; [V13 implementation](#public-implementations-and-evidence) for selective reuse; [V6](notes/v6/README.md) for integration foundations |
| Completion checks and restartable handoffs | [V12: Completion Integrity](notes/v12/README.md) — check what the next person or AI needs to resume | [V12 software and CI](#public-implementations-and-evidence), then [V13](notes/v13/README.md) for the next-cycle decision |
| Whether to continue, pause, limit, or rescale | [V13 research note](notes/v13/README.md) for GO / HOLD / CAP / BLOCK; [V10](notes/v10/README.md) if the goal itself is exhausting available capacity | [LoopKit](#public-implementations-and-evidence), then V11 → V12 for memory and completion |
| Safety and public-release judgment | [V5 Adoption Gate](notes/v5-addendum/README.md), then [V5 Revised](notes/v5/README.md) | [V9.1](notes/v9/README.md) for impact-weighted release and reuse; [V8](https://doi.org/10.5281/zenodo.19690553) for control over trajectories |
| Burden returned to humans at handoffs | [V14: Resource Justice](notes/v14/README.md) — who must reconstruct, verify, or repair when a transfer fails? | [V11](notes/v11/README.md) → [V12](notes/v12/README.md) → [V13](notes/v13/README.md) for the adjacent layers |
| Structural theory and research lineage | [V6: Canonical Commitment](notes/v6/README.md) → [V7 Final](notes/v7-final/README.md) → [V8](https://doi.org/10.5281/zenodo.19690553) | [V4](https://doi.org/10.5281/zenodo.17905930) for structural thinking; [chronological timeline](docs/research_timeline.md) for development history |

For a short evaluator checklist, use [START_HERE.md](START_HERE.md). The [notes directory guide](notes/README.md) routes to local manuscripts and supplements.

## Series index (Zenodo)

The **V-number identifies a research layer**; the **deposited version** identifies a publication within that layer. Titles below omit the repeated “Decision-OS” prefix. DOI links cite specific archived versions; local guides explain the available PDFs. “Published” below means a public deposit, not a claim of peer review.

| Layer and title | What it adds | Published form / deposited version | Formal citation and local reading |
| --- | --- | --- | --- |
| **V4 — Polaris-Origin: An Entry OS for Seeing Structure with AI** | Divergence and convergence as an entry to structural thinking | Paper; metadata type Text; version label not supplied | [DOI 17905930](https://doi.org/10.5281/zenodo.17905930) · [English PDF](notes/Decision-OS_V4_Polaris-Origin.pdf) |
| **V5 Revised (SiriusA2): A Zero-Knowledge Confirmation Layer for Trajectory-Aware Human–AI Decision Safety** | Confirmation, revoke paths, trajectory-aware pressure signals, and independent stop conditions | Preprint; `V5 Revised (SiriusA2)` | [DOI 19828435](https://doi.org/10.5281/zenodo.19828435) · [V5 guide and earlier editions](notes/v5/README.md) |
| **V6 (PIC): Canonical Commitment for Non-Destructive Integration** | Conditions for order-robust integration without diluting safety at commitment | Preprint; `V4` in deposit metadata; local filename says `v2` | [DOI 19433866](https://doi.org/10.5281/zenodo.19433866) · [V6 guide](notes/v6/README.md) |
| **V7 Final: Guardable Self-Recursive Evolution** | Structural failure boundaries for recursive updates; does not establish sufficient conditions for AGI | Preprint; `V7 Final EN v1.0` | [DOI 20422099](https://doi.org/10.5281/zenodo.20422099) · [V7 Final and earlier V7](notes/v7-final/README.md) |
| **V8: Time-Tube Control for Self-Safe AGI** | Evaluate trajectories, reversibility, drift, and dependency rather than a single output | Preprint; `v3` | [DOI 19690553](https://doi.org/10.5281/zenodo.19690553) · [English PDF](notes/v8/Decision_OS_V8_Time_Tube_Control_for_Self_Safe_AGI__EN２.pdf) |
| **V9.1: Impact-Weighted Release — From Continuous-Pass Gates to Condition-Bound Judgment Reuse** | As-of evidence, responsibility, sustained release checks, and reuse only while stored conditions remain valid | Preprint; `v9.1` | [DOI 19935535](https://doi.org/10.5281/zenodo.19935535) · [V9/V9.1 guide](notes/v9/README.md) |
| **V10: Recalculating Goal-Length Without Breaking the Carrier of Aspiration** | Rescale a goal before continuation destroys the capacity needed to pursue it | Full paper / preprint; `v2.0`; distinct from the earlier short Note | [DOI 20371623](https://doi.org/10.5281/zenodo.20371623) · [V10 guide](notes/v10/README.md) |
| **V11: Forget for Future — Reconnectable Forgetting for Long-Horizon Agentic AI** | Compress memory while preserving evidence, conditions, and re-entry paths | Full paper / working paper; `v2.0`; distinct from the earlier Note | [DOI 20301056](https://doi.org/10.5281/zenodo.20301056) · [V11 guide](notes/v11/README.md) |
| **V12: Completion Integrity** | Future-restartable closure; v2 adds completion-context contamination and a fresh evaluation requirement | Framework paper / preprint; `v2`; companion software is separate | [DOI 20370655](https://doi.org/10.5281/zenodo.20370655) · [V12 guide](notes/v12/README.md) |
| **V13 Research Note v0.2: Post-Optimization Survival Architecture — Compound Loop Governance for AI Operations** | Decide whether the next iteration improves future conditions: GO / HOLD / CAP / BLOCK | Research Note / working paper; `v0.2`, “Canon Freeze / Prototype-Bound Draft” | [DOI 20634743](https://doi.org/10.5281/zenodo.20634743) · [V13 guide](notes/v13/README.md) |
| **V14 Research Note: Resource Justice at the Joint Layer** | Track responsibility, temporal ownership, and human burden across transfers between contexts | Research Note / working paper; `v0.1`, timestamped draft; no full implementation architecture or benchmark | [DOI 21148211](https://doi.org/10.5281/zenodo.21148211) · [V14 guide and local PDF](notes/v14/README.md) |

Lineage reading is **V4 → V5 → V6 → V7 → V8 → V9/V9.1 → V10 → V11 → V12 → V13 → V14**. This is a conceptual route, not publication chronology or a requirement to read every paper. Revisions within V6, V7, and V9 have explicit archival relationships; larger series numbers do not make earlier layers obsolete. See [version relationships](docs/research_timeline.md#version-relationships).

### Addenda and Value Dynamics notes

| Artifact | Contribution / status | Citation and local guide |
| --- | --- | --- |
| V4 Addendum: Grounded Decision Protocol (V5-compatible Guard) | Published preprint; grounded GO / HOLD / NO protocol | [DOI 18469000](https://doi.org/10.5281/zenodo.18469000) · [guide](notes/v4-addendum/README.md) |
| V5 Addendum — SiriusA Adoption Gate (0.3 Disclosure) | Published preprint supplement; hold-first adoption check; “0.3 Disclosure” is in the title, not a supplied metadata version | [DOI 18252623](https://doi.org/10.5281/zenodo.18252623) · [guide](notes/v5-addendum/README.md) |
| V6 Addendum: Evaluation Hooks for PIC — Verification Note (1p) | Published preprint supplement; proposed tests and falsifiers, not a report of passed experiments | [DOI 18240015](https://doi.org/10.5281/zenodo.18240015) · [guide](notes/v6/README.md) |
| V7 Addendum V2: Why Aspire, Why PIC | Published preprint, `v2`; why direction and structural invariance are needed | [DOI 18896167](https://doi.org/10.5281/zenodo.18896167) · [guide](notes/v7-addendum/README.md) |
| Time-is-an-Ally V3 — Value as a Non-Decreasing Trajectory Under External Signals | Published preprint, `v3`; accumulation and externally triggered re-evaluation, not price forecasting | [DOI 19076241](https://doi.org/10.5281/zenodo.19076241) · [note](notes/time-is-an-ally/note.md) |
| Genesis Selection | Published preprint; accumulated value versus externally selected dominance | [DOI 19157058](https://doi.org/10.5281/zenodo.19157058) · [guide](notes/genesis-selection/README.md) |
| Value Dynamics Part III: Settlement Conditions of Value | Published preprint, `v1.0`; conditions for endurance after accumulation and selection | [DOI 20261794](https://doi.org/10.5281/zenodo.20261794) · [guide](notes/settlement-conditions/README.md) |

## Public implementations and evidence

**Paper proposals and software evidence answer different questions.** V11–V14 do not establish a complete self-evolving AI system. A schema check, an observed handoff, or a prototype stop condition supports only the tested behavior. The links below distinguish current software entry points from records pinned to the inspected code revision.

| Public implementation | What is available | Verification record and practical limit |
| --- | --- | --- |
| [V12 Completion Integrity](https://github.com/shin4141/decision-os-v12-completion-integrity) | Completion Record schema, CLI, examples, checklist, and CI; [installation guide](https://github.com/shin4141/decision-os-v12-completion-integrity/blob/main/docs/install-in-your-repo.md) | [Successful CI run 27920845535](https://github.com/shin4141/decision-os-v12-completion-integrity/actions/runs/27920845535) at `be1b3f7`; [workflow at that commit](https://github.com/shin4141/decision-os-v12-completion-integrity/blob/be1b3f70128d67e642d288c2bab9b53719720c37/.github/workflows/validate.yml) checks nine example records, including DELAY/BLOCK and declared/inferred output agreement. It checks record structure and restart handles, not the truth of evidence or code correctness. |
| [V13 LoopKit](https://github.com/shin4141/decision-os-v13-loopkit) | Operating prototype: V12→V13 next-loop reporting, handoff, selective external-memory reuse, and a bounded repository scanner. Start with [English onboarding](https://github.com/shin4141/decision-os-v13-loopkit/blob/main/docs/external_intelligence_onboarding.md) and the [reading order](https://github.com/shin4141/decision-os-v13-loopkit/blob/main/docs/ai_reading_order.md); inspect only relevant Field Notes (dated operating observations). | [Forward Use 003](https://github.com/shin4141/decision-os-v13-loopkit/blob/42e406e858b05b6b8aff5cc6669cf10ad506b424/examples/aspire_gap_forward_use_003/results.md) records note selection and a recommendation; [004](https://github.com/shin4141/decision-os-v13-loopkit/blob/42e406e858b05b6b8aff5cc6669cf10ad506b424/examples/aspire_gap_forward_use_004/results.md) records one patch in one private target. These are creator-owned bounded observations, not independent certification or broad adoption evidence. |
| [MMAR/L0 core](https://github.com/shin4141/mmar-l0-core) and [SiriusA core](https://github.com/shin4141/siriusA-core) | Related gate implementations producing PASS / DELAY / BLOCK artifacts; MMAR means Multi-Model / Multi-Rule Analysis. This repository's demo uses MMAR/L0 plus local policy annotations. | [Demo workflow](.github/workflows/decision-gate.yml) and [runs](https://github.com/shin4141/decision-os-paper/actions/workflows/decision-gate.yml). Rule-based synthetic scenarios do not validate the full V5 revised ZK/duress architecture or general real-world safety. |

Further V13 evidence, pinned to inspected public main `42e406e`:

- [Runner v0.2 External Validation Run 001](https://github.com/shin4141/decision-os-v13-loopkit/blob/42e406e858b05b6b8aff5cc6669cf10ad506b424/validation/v13_runner_v0_2_external_validation_run_001.md): 12 scans across three unrelated public repositories; repeated-output determinism and no-write checks passed. Usefulness was one useful, one partly useful, one not useful. Evaluation was internal; independent reproduction and generalization were not established.
- [Onboarding validation](https://github.com/shin4141/decision-os-v13-loopkit/blob/42e406e858b05b6b8aff5cc6669cf10ad506b424/validation/external_intelligence_onboarding_13_189.md): five focused tests and bounded fresh-context trials on a local candidate. The record leaves a fresh public-URL trial unverified and does not validate a new memory implementation.
- [Cycle 006 terminal failure record](https://github.com/shin4141/decision-os-v13-loopkit/blob/42e406e858b05b6b8aff5cc6669cf10ad506b424/validation/a7_creator_live_cycle_006_terminal_public_evidence_001.md): one attempt stopped at `A1_CAPTURE` with `A1_CANDIDATE_INDEPENDENCE_NOT_PASS`; no Note or real After was produced, and A2–A7 did not run. The file remains marked draft/publication approval pending. Its public presence and this link do not certify successful reuse, a complete Compactor, or release eligibility.

The [V12 software release `v2.2.3`](https://github.com/shin4141/decision-os-v12-completion-integrity/releases/tag/v2.2.3) and [V13 software release `v0.1.0`](https://github.com/shin4141/decision-os-v13-loopkit/releases/tag/v0.1.0) are software snapshots, not paper versions. V13's current main has evolved beyond that initial release; use its current README to navigate and fixed commits when describing an observation. Selective reuse does not update model weights, and a successful V12 check does not automatically authorize a V13 GO.

## Decision Gate demo (Actions)

[![Decision Gate](https://github.com/shin4141/decision-os-paper/actions/workflows/decision-gate.yml/badge.svg)](https://github.com/shin4141/decision-os-paper/actions/workflows/decision-gate.yml)

Open the [Decision Gate workflow](https://github.com/shin4141/decision-os-paper/actions/workflows/decision-gate.yml), choose a completed run, and open the `decision_gate` artifact containing `decision_gate.json`. Artifact download requires GitHub sign-in and depends on retention. To dispatch a run, use repository write access or a fork with Actions enabled.

The [workflow source](.github/workflows/decision-gate.yml) offers `pass`, `delay`, `block`, crypto, coordination, phishing, allowlist, and secrets scenarios. Inputs are synthetic; annotations inspect supplied fields, not live wallets, domains, or secrets. Manual runs can be green for any gate verdict; the badge reports workflow status, not safety approval. The workflow fetches the engine's moving `main`, so inspect the run's checkout revision when reproducing it.

Canonical engine contracts are in MMAR/L0: [decision_gate.schema.json](https://github.com/shin4141/mmar-l0-core/blob/main/decision_gate.schema.json) and [mmar_findings.schema.json](https://github.com/shin4141/mmar-l0-core/blob/main/mmar_findings.schema.json). For scope and adoption context, see the [policy semantics](docs/policy-pack-v5.md) and [template boundary](docs/adoption-github-actions.md).

## Terms and evaluation

- **Aspire / Carrier:** the continuing direction of a goal / the human, organization, resources, and recovery capacity that sustain it.
- **As-of / Seat:** the evidence and conditions at a specified time / the holder of decision rights and responsibility.
- **PIC / canonical commitment:** Phase-Invariant Core; integrating admissible updates under declared invariants so update order does not change the committed result.
- **Residue / re-entry:** selected decision-relevant structure retained from prior work / a path back to its source, conditions, and unresolved issues.
- **Joint layer:** a transfer point between sessions, agents, tools, files, or repositories where state and responsibility must continue.

For human or AI evaluation, follow **claims → assumptions → dependencies → check type → falsifier → summary**. Label each claim as a definition, conditional theoretical result, operational proposal, or bounded empirical observation. A confident summary is not evidence; inspect the cited paper and, for implementation claims, the relevant code and result record.

## Citation and historical anchors

Cite the **specific paper's version DOI** from the index. A concept DOI groups versions of one work; it is not a DOI for the whole Decision-OS series. [CITATION.cff](CITATION.cff) provides structured references. Its gateway release date is historical repository metadata, not the date of every paper. For software claims, cite the implementation repository and the inspected commit or release as well.

Older “SSOT” (single source of truth) labels below are **historical fixation anchors only**, not authority over today's entire series:

- V5-era ProjectFiles `v2025-11-03`: [DOI 17511725](https://doi.org/10.5281/zenodo.17511725); original abbreviated `SHA256=0941d922...` retained as recorded, not a complete verifiable hash.
- Genesis [DOI 17480645](https://doi.org/10.5281/zenodo.17480645), *SiriusA: Choose the Operating Point*: earlier README associated commit `840c85de344f5dd197dc5122ad9f4ba452f2970d` with that PDF. Byte identity was not reverified here.
- V8 `v2` [DOI 18137204](https://doi.org/10.5281/zenodo.18137204): earlier README recorded `a771021949fabf4b0ea23141863bab5f1a266e8c`. This does not identify V8 `v3` or later papers.
- [Evidence of 2025-11-04](evidence/2025-11-04/README.txt), [manifest](evidence/manifest.json), and commit [`991d81e2a7`](https://github.com/shin4141/decision-os-paper/commit/991d81e2a7531ae6ab565ce2ced77ed2605fda6f) remain dated evidence records, not a current validation certificate.

The [research timeline](docs/research_timeline.md) preserves the publication sequence and edition relationships. [This gateway update record](docs/gateway_update_2026-09-13.md) records sources, validation limits, and rollback. Original papers, PDFs, evidence, hashes, releases, and tags are preserved.

Author: **Shinichi Nagata**, Independent Researcher, Kanagawa, Japan. See [Author's Note](AUTHORS_NOTE.md), [license](LICENSE), and [optional tools](notes/tools.md). Contact: **siriusa.paper@gmail.com** · [DecisionOS on X](https://x.com/DecisionOS).
