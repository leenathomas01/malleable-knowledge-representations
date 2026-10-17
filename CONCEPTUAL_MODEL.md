# Conceptual model — before choosing a substrate

**This document preserves the origin of the proposal, not an established scientific theory.**

## Four complementary metaphors

- **Lego / W:** A useful composition becomes a first-class component. A composite can be made in different ways, provided those ways meet the *relevant* behavioral requirements.
- **Ropes:** Relations and partial constructions may be intertwined, detached, spliced, and reassembled without committing to one permanent partition.
- **Clay:** A partially specified intention influences construction, but discoveries during construction may also reshape the intention. This is a hypothesis about exploration, not a license for an agent to disregard assigned goals.
- **Compiler:** Repeated structures or trajectories may be consolidated for more efficient reuse. Compression can save work but can also hide failures and erase future-relevant distinctions.

## Candidate mechanism, not a mandatory ontology

An abstraction W may be a stored object, a generator, a learned procedure, a region or transformation in latent space, a contextual equivalence class, or a reconstructed process. These representations are **alternatives**; there is no evidence they are all equivalent.

A composition `W = compose(a,b,c,d,e)` might later be replaced by `W' = compose(p,q,r)`. Equivalence requires specifying a task family and probes. Agreement under one context does not imply unrestricted substitutability.

A learned trajectory may also become reusable, yet its preconditions, intermediate dependencies and failure modes matter. A sufficiently capable system could operate at a higher abstraction level without reperforming all lower-level steps, but only when this reuse is valid and cheaper than recomputation.

## Human understanding

Internal representations need not be translated into prose to be useful. Conversely, no principle excludes mathematical, geometric, intuitive, or symbolic interfaces that humans can use. Interpretability varies by representation, observer, task, and interface. Functional understanding should be tested through predictions, interventions and robustness—not inferred from compelling explanations.

## Dynamic play

Exploration may be partially open-ended: retrieve, deform, compose, test, consolidate and revisit possibilities before immediate utility is known. A practical autonomous agent still requires explicit constraints, evaluation, and control over whether suggested objective revisions are adopted.

## Separate speculative extensions

Changing granularity; contextual equivalence; composable latent trajectories; generative rather than purely predictive compression; and goals influenced by discovery are **different claims**. They should be tested separately rather than bundled into a single success condition.
