# 2. Hunt for measurable performance wins

```text
Find and implement performance improvements in this repository.

Identify important user flows and expensive operations. Use available profiles, traces, query plans, browser tooling, or benchmarks to locate bottlenecks. If I have not named a priority, choose representative flows from the repository and explain the choice.

Establish a reproducible baseline before editing. Record the workload, dataset, environment, revision, and relevant measurements. If tooling is missing, add the smallest useful harness with existing tools.

Prioritize repeated work, unnecessary requests, N+1 queries, avoidable allocations, large payloads, and inefficient algorithms where measurements show an opportunity. Choose an improvement, implement it, and compare before and after under equivalent conditions.

Repeat measurements enough to assess noise. Include relevant tradeoffs such as memory, throughput, tail latency, freshness, and failure behavior. Check correctness as well as timing.

Keep changes that improve the measured result while preserving correctness. Revert failed experiments. If an experiment still simplifies the code, report that benefit without claiming a speedup.

Report before/after measurements, reproduction commands, correctness checks, and remaining bottlenecks. Label results limited to synthetic workloads or local hardware. If you cannot measure a proposed speedup, say so and name the tool or access you need.
```
