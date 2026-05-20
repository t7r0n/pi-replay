# Decision Report: Pi Replay

A deterministic replay + OTel tracing harness for pi worker agents - record every tool call, child Worker invocation, and Durable Object state diff; replay any session bit for bit; enforce per session budgets in the Worker runtime.

## Evidence-Grounded Findings

CLAIM: claim regression harness should `open a regression issue with trace and benchmark delta` because blocks=3 reviews=5 mean_severity=2.528. [EVID: ev_0066]
CLAIM: evidence replay should `block release until cited evidence is regenerated` because blocks=4 reviews=5 mean_severity=2.611. [EVID: ev_0044]
CLAIM: handoff boundary probe should `route to reviewer with evidence packet` because blocks=3 reviews=4 mean_severity=2.528. [EVID: ev_0077]
CLAIM: review operator packet should `accept only if decision claims cite fixture evidence` because blocks=4 reviews=5 mean_severity=2.556. [EVID: ev_0011]
