# 13. Plan a new feature or build from scratch

```text
Create an implementation plan for this idea:
[describe the idea, problem, desired outcome, or selected opportunity and research brief from prompt 14]

Context, if known:
- Existing project or new project: [details]
- Intended users and primary use case: [details]
- Constraints: [requirements, budget, deadline, integrations, or preferences]

Plan this work before implementation. You may inspect available code and documentation and save the planning document. This task overrides the shared permission to change application code or environments; leave implementation, dependency installation, external writes, and deployment for a subsequent implementation request.

For an existing project, inspect its architecture, relevant flows, conventions, and verification tools. Ground the plan in actual code and identify what can be reused. Distinguish discovered file paths from proposed new files.

For a new project, define the users, problem, and smallest useful first release. Recommend a simple stack based on the requirements. Verify current compatibility and service constraints in official sources when they affect the recommendation.

If the idea is exploratory, suggest up to three concrete directions, explain their value and main tradeoff, and recommend one. If I have defined the outcome, plan it. Ask up to three questions if the answers would change scope or architecture. Continue planning independent parts and mark unresolved decisions.

Prefer the simplest design that meets the requirements. Preserve explicit requirements and define what the first release excludes. Avoid infrastructure or abstractions justified only by hypothetical future scale. For an unproven approach, plan a small feasibility check and define the result you need before committing to it.

Produce:
1. The user problem, intended outcome, and observable success criteria.
2. First-release scope, non-goals, assumptions, and unresolved decisions.
3. The recommended approach, including relevant user flows, components, data, and integrations. Include alternatives only where a real tradeoff warrants a choice.
4. Ordered implementation milestones. For each, state the working behavior delivered, affected areas, dependencies, and completion checks. Start with the smallest useful end-to-end flow. Identify work suitable for separate parallel tasks and work that must remain sequential.
5. A verification plan mapped to acceptance criteria, including required tools, access, test data, and relevant failure cases. Include security, accessibility, performance, or migration checks where the feature requires them.
6. Rollout and recovery steps where relevant, concrete risks, and decisions that block implementation. State the assumptions behind any rough estimates.
7. A copyable prompt for the first implementation task, carrying its objective, context, scope, dependencies, and acceptance criteria into a fresh session.

Scale the plan to the work: a small feature may need only a few paragraphs. Save one planning document in the established project location, or an appropriate output location if no convention exists, and link it. Finish after delivering the plan; implementation begins when I request it.
```

After reviewing the plan, pass it to prompt 12 or run the implementation prompt from the plan.
