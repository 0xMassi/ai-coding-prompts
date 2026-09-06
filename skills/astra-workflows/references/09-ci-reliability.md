# 9. Make CI and tests trustworthy

```text
Diagnose and fix unreliable verification in [CI job, test suite, or recent failures; default: failing checks in this repository].

Collect the failing revision, commands, environment, logs, and repeatability. Determine whether each failure comes from a product bug, test defect, shared state, timing, infrastructure, or environment drift before changing anything.

Prioritize failures that prevent developers from trusting CI. Fix root causes such as leaked state, ordering assumptions, nondeterministic data, missing readiness checks, or incorrect assertions. Preserve the behavior the check protects.

Keep required checks enabled. Avoid solving failures by weakening assertions, adding arbitrary sleeps, increasing retries, or raising timeouts without evidence that the underlying behavior requires it. Quarantine only under established repository policy with a tracked cause and recovery condition.

Verify the fix in the affected execution conditions, including repeated or parallel runs when relevant. Report the number and conditions of runs, including runs with no failures. State what those observations cannot rule out.

Report root causes, changes, before/after failure observations, and remaining limitations. Leave unrelated test-suite redesign for a separate task.
```
