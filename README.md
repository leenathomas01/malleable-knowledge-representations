# Malleable Knowledge Representations (MKR)

**Status:** Speculative, open research proposal · **Results:** None claimed · **Started:** 2026-10-17

Can knowledge representations be dynamically reorganized, recombined, and reused as contexts change—without assuming permanently fixed abstraction boundaries?

This repository preserves a **broad conceptual possibility** alongside a **narrow, falsifiable experimental proposal**. They must not be mistaken for one another.

## The central intuition

A useful structure, relation, or previously traversed process may become a reusable abstraction (provisionally **W**). A wall assembled from five pieces may function as one component in a later construction; a different three-piece realization may serve the same *specific* purpose; a successful trajectory might become an operator. Such substitutions are always conditional on context and testing.

The analogy extends to mutable organization: compositions may be split, combined, reconstructed, or selectively reused. A loosely specified goal might also evolve through exploratory interaction with available components. Representations need not be exclusively discrete, symbolic, human-readable, or fixed-dimensional.

**This is a hypothesis-generating intuition, not evidence that a model currently supports arbitrary latent rewriting or causal understanding.**

## Scope boundaries

- **Conceptual track:** [CONCEPTUAL_MODEL.md](CONCEPTUAL_MODEL.md) records the expansive idea, including dynamic play and partially specified intentions.
- **Research track:** [research/reshape.md](research/reshape.md) proposes a *bounded*, optional, reversible `reshape()` call that returns candidates for assessment.
- **Empirical track:** [experiments/001-reshape-baselines.md](experiments/001-reshape-baselines.md) designs a controlled test against strong baselines, with full cost accounting.

No specific computational substrate is required by the conceptual proposal. Symbolic refactoring, latent-space transformations, trajectory abstraction, and localized model adaptations are *potential implementation families*, not interchangeable proofs of a unified mechanism.

## Two independent questions

1. Can a system produce valid, useful changes to its current representational organization (rather than only adding more stored units)?
2. Does access to such transformations measurably improve performance, transfer, or efficiency over conventional retrieval, refactoring, additional search, or equivalent training compute?

An affirmative answer to the first does not imply the second.

## Research materials

- [CONCEPTUAL_MODEL.md](CONCEPTUAL_MODEL.md) — original intuition and scope
- [HYPOTHESES.md](HYPOTHESES.md) — operational claims and disconfirmation
- [research/reshape.md](research/reshape.md) — callable interface, trust boundaries
- [experiments/001-reshape-baselines.md](experiments/001-reshape-baselines.md) — minimum discriminating test
- [literature/README.md](literature/README.md) — nearest existing work and caveats
- [LIMITATIONS.md](LIMITATIONS.md) — known problems and nonclaims
- [OPEN_QUESTIONS.md](OPEN_QUESTIONS.md) — uncommitted future possibilities
- [CONTRIBUTING.md](CONTRIBUTING.md) — evidence and contribution standards

## Research posture

We do **not** claim invention of library learning, options, compiler refactoring, latent arithmetic, model merging, modular adapters, or program synthesis. No empirical results have been produced for MKR. Cite primary evidence when making factual claims; leave unverifiable assertions marked as conjecture.

This exploratory framing emerged through human–AI discussions, including critical analysis and bibliography suggestions from multiple assistants. All paper-specific details require independent verification before formal academic citation.

## Related proposal

[Capability–Substrate Decoupled Exploration](https://github.com/leenathomas01/capability-substrate-exploration) explores preservation and reassessment of unrealized ideas. MKR instead investigates *representation reorganization*. The projects share a philosophy but test different claims.
