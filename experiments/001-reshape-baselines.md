# Experiment 001 — Optional restructuring versus strong baselines

**Status:** Preregisterable design, not executed.

## Question

Can a bounded optional representation transformation improve post-shift compositional task performance beyond extra computation, ordinary retrieval, and conventional adaptive refactoring?

## Small world

Use generated short programs (or 8–12 primitive block-world actions) built from shared substructures. Split training and held-out tasks by *compositions*, not random examples. Midway through evaluation, change one operation's context-specific validity or cost, without revealing the new test cases. Maintain a frozen base model where applicable.

## Conditions

- **A:** No restructure; extra search/reasoning budget equal to treatment's entire call cost.
- **B:** Competent program library: reusable fragments, caching, invalidation and conventional refactoring.
- **C:** Fixed latent/operator reuse with the same input information.
- **D:** Optional `reshape()` proposes local re-factorings or alternative decompositions; the caller evaluates and may veto.
- **E (ablation):** Reshape with shuffled validity context or disabled equivalence probe.

If D performs better than a deliberately frozen add-only cache but not B, evidence is for ordinary refactoring, **not a distinct MKR effect**.

## Prespecified shift and perturbations

Introduce mild representation drift (where meaningful), incomplete validity probes, near-match retrieval, and 1–5% context-specific operator changes. Randomize conditions and worlds independently. Register perturbation magnitude before testing.

## Metrics and fairness

**Primary:** held-out post-shift success rate under identical full budgets.

**Secondary:** cost per correct solution, transfer to unseen combinations, number of false equivalences, invalidations, rollback rate, and pre-shift retention. Account for candidate generation, probe creation/execution, retrieval, memory, validation, and adaptation. Avoid a protocol that gives only D extra evaluation information.

Use many independent generated worlds and seeds; report uncertainty intervals and null results. Controls must be able to detect a seeded positive restructuring effect.

## Decision rule

A positive result for H2 requires robust benefit of D over the strongest well-resourced baseline after full cost accounting and comparable information access. Null or negative effects constrain this variant, not every form of malleable representation.

## Safety and scope

Use toy, benign tasks. No automatic deployment of parameter updates, autonomous code changes to production systems, or unsupervised persistence of speculative candidates.
