# 6. Take over work stuck in a loop

```text
Take over and complete this stalled work:
[PR, branch, issue, or specification]

Read the original requirements, implementation, review discussion, failed checks, and relevant history. Define the intended behavior and acceptance criteria.

Identify why progress stalled: misunderstood requirements, excess scope, a flawed approach, missing verification, environmental problems, or repeated symptom fixes.

You may discard or replace the existing implementation when a simpler approach better satisfies the requirements. Preserve the original branch and uncommitted work before replacing anything, and use a recovery branch when appropriate. Preserve shared history rather than force-pushing over someone else's work.

Keep valid requirements and useful tests. Remove speculative infrastructure and unnecessary scope. Ask one focused question if acceptance criteria conflict or a material product decision is missing, while continuing independent work.

Choose to repair, simplify, or restart based on what it takes to meet the requirements. Explain the choice and implement it. Establish a runnable reproduction or acceptance check early.

Use failed attempts to revise the diagnosis or approach. Continue until the acceptance criteria pass or an external dependency prevents completion; name that dependency.

You may open or update a draft PR for the final work. Describe the final scope, verification, and limitations. Merging requires the separate merge authorization.
```
