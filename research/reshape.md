# Callable reshape() — bounded operation hypothesis

**Status:** Interface sketch; no working implementation or validated effect.

Instead of creating an end-to-end knowledge system, let an existing model or agent optionally request a bounded transformation of a *working representation*. The caller retains control of acceptance, persistence, and objective choice.

```python
candidate = reshape(
    workspace,                   # bounded input: programs, trajectories or accessible latents
    context,                     # task and validity context
    objective=None,              # None permits exploratory candidate generation
    budget=None,                 # explicit resource ceiling
    constraints=None             # allowed operations and safety policy
)
assessment = evaluate(candidate, held_out_probes)
if assessment.passes:
    caller_may_adopt(candidate)
```

The pseudocode describes an interface, **not a provided software package**.

## Invariants of the interface

1. **Bounded:** transformations act only on a supplied, permissioned workspace.
2. **Non-destructive by default:** return candidates without modifying backbone weights or the authoritative knowledge store.
3. **Inspectable provenance:** record source version, transformation family, cost, affected context, and what was or was not preserved.
4. **Separate proposal and validation:** candidate generation must not see held-out acceptance probes.
5. **Veto and rollback:** acceptance is the caller's decision; failure leaves original state available.
6. **Accounting:** compare value added with equivalent extra reasoning, retrieval, refactoring, or gradient steps.

## Plausible implementation families

- **Symbolic:** extract a reusable function/program from repeated structure, with equivalence tests.
- **Trajectory:** propose macro-actions or reusable subsequences subject to context-bound success probes.
- **Latent geometric:** transform activations in an identifiable task-relevant subspace, then test behavior. Embedding distance is *not* guaranteed functional equivalence.
- **Localized parameter update:** produce and validate a reversible adapter or low-rank patch. This may primarily add capacity rather than reorganize existing knowledge.

These are distinct methods; none is established as a universal reshape mechanism.

## Candidate record

`{source, transform_type, target_context, assumptions, validation_scope, held_out_score, compute_cost, memory_cost, rollback_ref, uncertainty}`

## Risks

Proxy improvement may diverge from actual downstream benefit. A temporary workspace does not prevent inaccurate outputs from influencing the caller after adoption. Unconstrained self-directed goal changes are outside this interface.
