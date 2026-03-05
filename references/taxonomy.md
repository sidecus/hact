# Preference Taxonomy

Use this taxonomy to cluster history signals into stable collaboration preferences.

## Categories

- `ownership-boundaries`
  - Signals: clear state ownership, no hidden coupling, cross-domain mutation concerns.
- `orchestration-thinness`
  - Signals: runtime/facade/proxy should stay thin; logic belongs in domain services/use-cases.
- `contracts-typing`
  - Signals: strict models, explicit validation, dislike of generic dict/json payloads.
- `simplicity-cognitive-load`
  - Signals: remove stale/dead code, avoid duplicate types, rename confusing entities.
- `flow-consistency-reuse`
  - Signals: align similar flows, reduce drift between parallel paths, maximize reusable logic.
- `ux-clarity`
  - Signals: readability, step order, reduced clutter, easier comprehension for target users.
- `process-rigor`
  - Signals: tests with refactors, docs stay aligned with implementation, explicit quality bar.

## Scoring

For each candidate preference, score:

- `frequency`: repeated across sessions
- `recency`: appears in latest sessions
- `explicitness`: direct commands/preference statements

Prioritize high score in at least two dimensions.

## Exclusion Rules

Do not treat as stable preference:

- one-off convenience asks
- tool/runtime artifact noise
- boilerplate or injected instruction blocks
- repeated retries caused by transient errors
