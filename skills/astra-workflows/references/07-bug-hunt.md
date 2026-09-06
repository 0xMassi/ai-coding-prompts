# 7. Hunt for bugs and fix their root causes

```text
Find and fix correctness bugs in [scope; default: important flows in this repository].

Identify intended behavior from requirements, contracts, callers, and existing tests. Prioritize concrete failures in state transitions, boundaries, concurrent operations, retries, cancellation, partial failure, and data persistence where applicable.

For each suspected bug, reproduce the failure or trace the code path that demonstrates it. Distinguish confirmed bugs from plausible concerns. Trace the root cause and affected callers before editing.

Group fixes by root cause and preserve unrelated code. Add the smallest meaningful regression check and demonstrate that it fails before the fix and passes afterward where feasible. Verify neighboring behaviors that share the cause.

Use local or isolated environments for failure injection and test data. Do not treat undocumented product choices as defects; ask if the intended behavior would change the fix.

For each confirmed bug, report its trigger, impact, root cause, fix, and regression check. List unverified suspicions and the scope you inspected.
```
