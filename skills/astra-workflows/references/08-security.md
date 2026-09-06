# 8. Review security boundaries and repair confirmed gaps

```text
Review security in [scope; default: externally reachable paths in this repository] and fix confirmed vulnerabilities within that scope.

Map the relevant entry points, identities, sensitive operations, data, and trust boundaries. Inspect authentication, authorization, tenant isolation, input handling, secrets, file access, outbound requests, and sensitive logging where applicable.

For each finding, describe the concrete path from attacker-controlled input to unauthorized behavior, the prerequisites, and the impact. Validate it with local or isolated tests using synthetic data. Keep hypotheses separate from demonstrated findings; check how the application uses the affected code before assigning impact.

Implement focused fixes that preserve intended access. Test both the legitimate operation and the denied case, including cross-user or cross-tenant cases where relevant. Keep validation at the boundary that owns the rule.

This task authorizes repository changes and isolated testing. Active probing of live third-party or production systems, credential rotation, and production data changes require separate authorization. Use source inspection and local reproductions to continue useful work.

Rank confirmed findings by impact. Include code locations, fixes, checks, and unresolved assumptions. State the scope you inspected and its coverage limits.
```
