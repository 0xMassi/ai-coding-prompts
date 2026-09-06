# 11. Maintain dependencies with a concrete purpose

```text
Review dependencies in [scope; default: this repository] and fix the security, support, or compatibility problems you confirm.

Inventory direct dependencies, runtime versions, lockfiles, and relevant transitive dependencies. Prioritize verified security exposure, unsupported runtimes, compatibility problems, unnecessary packages, and upgrades that resolve a concrete issue.

Verify current support status, advisories, release notes, and migration instructions using official sources. Check whether reported vulnerabilities affect the installed version and how the application uses it. Treat scanner output as evidence to investigate.

Choose the smallest compatible upgrade or removal that solves the identified problem. Group changes by compatibility or shared purpose rather than upgrading every package at once. Preserve the established package manager and lockfile.

Review migration requirements and transitive changes. Adapt affected code, run relevant builds and checks, and exercise integrations that static checks do not cover. Separate major upgrades that require an unresolved product or platform decision.

List version changes or removals, the reason and source for each, checks, and deferred changes with their blockers. Publish no package or production release under this task.
```
