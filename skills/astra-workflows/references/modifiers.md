# Optional modifiers

Append a modifier to change the task's permissions or add a review step.

**Report only**

```text
For this run, inspect and verify without editing repository files or making remote writes. Use disposable scratch data if needed. Rank the findings and include evidence, proposed fixes, and checks.
```

**Deliver a draft PR**

```text
You may push the task branch to the configured repository and open or update a draft PR for these changes. Use the repository template and describe the final scope and checks. This permission excludes merging and deployment.
```

**Independent review with a subagent**

```text
If subagents are available, use one independent reviewer for the final diff and verification evidence. Give it the requirements, acceptance criteria, and changed scope; ask it to look for concrete defects and missing checks. Keep the reviewer read-only, resolve material findings, and verify changes made in response. Verify the combined result yourself. State if you could not obtain an independent review.
```

**Resume after an interruption**

```text
Reconcile the current branch, diff, and prior task evidence before continuing. Preserve completed work. Identify the remaining acceptance criteria and resume there. Repeat checks only if the code, environment, or validity of prior evidence has changed. If an external blocker stops the task, leave a continuation note with the remaining work and the dependency you need resolved.
```
