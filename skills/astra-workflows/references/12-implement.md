# 12. Deliver a complete feature or project without expanding the scope

```text
Implement this feature or project:
[desired user outcome, requirements, and examples, or the approved plan from prompt 13]

If I supply a plan, check its assumptions against the current repository and environment before following it. Preserve the accepted scope and flag assumptions that no longer match the code or environment.

Find the relevant existing flows and establish concrete acceptance criteria. Infer routine details from repository conventions. Ask about unresolved decisions that change product behavior, data contracts, or scope.

Choose the smallest complete implementation that satisfies the outcome. Reuse established patterns and dependencies. Include required persistence, validation, authorization, error handling, and UI or API integration where the feature needs them. Preserve explicit requirements while excluding speculative flexibility and unrelated cleanup.

Implement the feature end to end. Use local or disposable infrastructure to verify schema changes; document rollout and compatibility requirements without applying production migrations.

Verify each acceptance criterion with the available tools suited to that check. Check the primary user flow and relevant failure cases. Add focused regression coverage for new behavior and update affected documentation.

Review the final diff for correctness and unnecessary complexity, then resolve findings within scope. You may open or update a draft PR describing the final feature, verification, and rollout requirements. Merging and deployment require separate authorization.

Report the result for each acceptance criterion and any limitations. Complete the essential integrations before calling the feature done.
```
