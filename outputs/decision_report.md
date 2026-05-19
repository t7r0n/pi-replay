# Decision Report: Pi Replay

A deterministic replay + OTel tracing harness for pi worker agents - record every tool call, child Worker invocation, and Durable Object state diff; replay any session bit for bit; enforce per session budgets in the Worker runtime.

## Evidence-Grounded Findings

CLAIM: isolation failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: lives gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0143]
CLAIM: lives reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0121]
CLAIM: observability policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0099]
CLAIM: worker drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0088]
CLAIM: worker evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0066]
