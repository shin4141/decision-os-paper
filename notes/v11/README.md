# Decision-OS V11: Forget for Future

**Reconnectable Forgetting for Long-Horizon Agentic AI**  
Author: **Shinichi Nagata**

## One-line thesis

**Future requires forgetting, but forgetting must remain reconnectable.**

## Why this matters

Long-horizon AI agents do not fail only because they forget.

They also fail because they remember in the wrong form.

As AI systems begin to operate across long conversations, files, tool calls, code changes, summaries, and handoffs between sessions, memory becomes both a capability and a burden. More memory can help in the short term, but over time it can create new failure modes:

- old assumptions re-enter new judgments;
- summaries replace original evidence;
- unresolved conditions become hidden premises;
- stop conditions weaken into ordinary notes;
- prior outputs become the next premise;
- long context becomes polluted rather than useful.

V11 calls this failure:

> **self-referential premise corrosion**

The problem is not simply “how can AI remember more?”  
The deeper question is:

> **When should an AI stop carrying full context, compress it, and preserve only what future judgment needs?**

## Core idea

V11 introduces **Reconnectable Forgetting**.

Forgetting is not deletion.  
Forgetting is not ordinary summarization.  
Forgetting is not losing the past.

In V11, forgetting means:

> **controlled compression that preserves the path back.**

A memory may leave active context only if the future evaluator can still reconnect to:

- the claim or decision;
- the evidence anchor;
- the As-of condition;
- the original scope;
- the stop or recheck condition;
- unresolved deltas;
- the re-entry path.

## What V11 contributes

### 1. Three-layer memory architecture

V11 separates long-horizon memory into three roles:

1. **Active Context Layer**  
   Current high-resolution working context.

2. **Compressed Residue Layer**  
   Claims, decisions, deltas, stop conditions, and reusable judgment structure.

3. **Provenance-Key Layer**  
   Source references, As-of timestamps, hashes, evidence pointers, and re-entry keys.

The goal is not to store everything.  
The goal is to know what can leave active context without breaking future re-entry.

### 2. Decision-Equivalent Compression

A compressed memory is not safe merely because it sounds similar to the original.

It is safe only if it preserves the judgment-critical structure needed to recover the same or safer decision state.

V11 distinguishes:

- **meaning preservation**: does the compressed memory say something similar?
- **judgment preservation**: can it still support safe future decision-making?

### 3. Reconnectability Gate

Compressed memory should not be reused directly.

V11 introduces a gate with three outputs:

- **PASS** — reusable as judgment material;
- **DELAY** — needs recheck or re-anchor;
- **BLOCK** — must not be used as a judgment ground.

The gate checks:

- Origin Identity
- Judgment Fidelity
- Resolution Fitness
- Difference Recoverability

### 4. Outcome-Masked Replay Test

To test whether compression preserved judgment fidelity, the future evaluator hides the original outcome and tries to reconstruct the gate-relevant state using only:

- the compressed memory;
- its evidence anchor;
- declared judgment-critical queries.

If the evaluator can recover the same or safer PASS/DELAY/BLOCK state, the compression is usable.  
If not, the missing condition must be identified and repaired.

### 5. Adaptive Handoff Window

V11 also asks **when** an active context should be handed off.

The handoff point is not fixed.

- Failed or polluted contexts should be closed early.
- Normal contexts may be handed off at convenient work boundaries.
- High-value coherent contexts may be extended longer.
- High-impact or irreversible material should be anchored earlier.

This makes V11 a practical framework for long conversations, agent workflows, AI coding sessions, research logs, and multi-session handoffs.

## Key distinction

V11 is not a paper about making AI remember everything.

It is a paper about preventing memory from becoming a hidden source of future failure.

> **A readable summary is not enough. A memory is usable only if future judgment can reconnect to its source, scope, conditions, and stop rules.**

## Relation to the Decision-OS series

- **V9** fixed As-of, Seat, and Release: how past decisions should be reviewed without hindsight collapse.
- **V10** asked how an agent survives by rescaling goals without betraying aspiration.
- **V11** asks what the surviving agent can stop carrying in full while preserving future re-entry.
- **V12** asks when work may be closed without breaking the future self.

In short:

> **V11 governs what may be forgotten. V12 governs what may be closed.**

## Files

- [`Decision_OS_V11___Forget_for_Future.pdf`](./Decision_OS_V11___Forget_for_Future.pdf) — full English paper
- [`Decision_OS_V11_Note_Forget_for_Evolution_V1.pdf`](./Decision_OS_V11_Note_Forget_for_Evolution_V1.pdf) — earlier short note

## Suggested citation

```bibtex
@misc{Nagata2026DecisionOSV11,
  author = {Shinichi Nagata},
  title  = {Decision-OS V11: Forget for Future -- Reconnectable Forgetting for Long-Horizon Agentic AI},
  year   = {2026},
  note   = {Decision-OS research sequence}
}
```

## Status

This paper is a conceptual and operational framework.  
It does not claim empirical validation, deployment testing, or implementation as a complete memory architecture.

The goal of V11 is narrower:

> to define the minimum conditions under which forgetting can reduce context burden without destroying future re-entry.

V11 should be read as a design primitive for long-horizon agentic AI memory, not as a finished memory product.
