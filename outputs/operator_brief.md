# Operator Brief: camelAI

camelAI gets a local, deterministic pressure test around worker, lives, and isolation. The useful part is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- worker evidence replay -> block release until cited evidence is regenerated (worker_coverage, evidence ev_0000).
- observability operator packet -> accept only if decision claims cite fixture evidence (lives_risk, evidence ev_0143).
- isolation regression harness -> open a regression issue with trace and benchmark delta (isolation_precision, evidence ev_0066).
- lives boundary probe -> route to reviewer with evidence packet (observability_latency, evidence ev_0033).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.
