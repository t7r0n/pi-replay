# Failure Matrix: Pi Replay

| Scenario | Failure mode | Metric | Gate | Evidence |
| --- | --- | --- | --- | --- |
| worker evidence replay | worker_drift | worker_coverage | block release until cited evidence is regenerated | ev_0000 |
| observability operator packet | observability_blindspot | observability_latency | accept only if decision claims cite fixture evidence | ev_0007 |
| observability operator packet | observability_blindspot | observability_latency | accept only if decision claims cite fixture evidence | ev_0011 |
| isolation regression harness | isolation_misroute | isolation_precision | open a regression issue with trace and benchmark delta | ev_0014 |
| lives boundary probe | lives_gap | lives_risk | route to reviewer with evidence packet | ev_0021 |
| isolation regression harness | isolation_misroute | isolation_precision | open a regression issue with trace and benchmark delta | ev_0022 |
| worker evidence replay | worker_drift | worker_coverage | block release until cited evidence is regenerated | ev_0028 |
