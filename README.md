# Pi Replay

A deterministic replay + OTel tracing harness for pi worker agents - record every tool call, child Worker invocation, and Durable Object state diff; replay any session bit for bit; enforce per session budgets in the Worker runtime.

## Why This Exists

pi worker lives or dies on isolation, observability, and the execute tool's reliability - but the README explicitly says the repo is "actively experimental" and only the terminal agent example is production ready. The execute tool uses Cloudflare's Dynamic Worker Loader to spin up a child Worker per code execution, but two things are missing from the public surface: (1) deterministic replay - when a pi style agent's run fails, there is no built in way to replay the exact sequence of tool calls + Worker invocations.

## What It Builds

- Replays synthetic `worker` and `lives` cases against the project's evidence rules.
- Scores `worker_coverage`, `lives_risk`, and `isolation_precision` so regressions are visible in CSV and JSON.
- Plants `worker drift` and `lives gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `pi-replay` without hosted services.

## Local Run

```bash
uv sync
uv run pi-replay all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://github.com/qaml-ai
- https://github.com/qaml-ai/pi-worker
- https://github.com/qaml-ai/camelAI-docker-compose
- https://www.ycombinator.com/companies/camelai
- https://blog.cloudflare.com/durable-object-facets-dynamic-workers/
- https://linkedin.com/in/illiana-reed

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
