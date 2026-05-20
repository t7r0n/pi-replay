# Pi Replay

A deterministic replay + OTel tracing harness for pi worker agents — record every tool call, child Worker invocation, and Durable Object state diff; replay any session bit for bit; enforce per session budgets in the Worker runtime.

![Pi Replay working dashboard](outputs/project_working.svg)

## Why it exists

pi worker lives or dies on isolation, observability, and the execute tool's reliability — but the README explicitly says the repo is "actively experimental" and only the terminal agent example is production ready. The execute tool uses Cloudflare's Dynamic Worker Loader to spin up a child Worker per code execution, but two things are missing from the.

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/pi_replay/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Pi Replay evidence map](outputs/evidence_map.svg)

## Signals it measures

- `worker coverage`
- `lives risk`
- `isolation precision`
- `observability latency`

## Failure modes it plants

- worker drift
- lives gap
- isolation misroute
- observability blindspot

## Run it locally

```bash
uv sync
uv run pi-replay all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
