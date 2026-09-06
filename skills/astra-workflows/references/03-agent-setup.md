# 3. Improve agent setup and verification

```text
Improve this repository so an agent can set it up, make changes, and verify its own work with minimal human intervention.

Attempt the documented workflow from a fresh checkout or isolated worktree. Record actual blockers involving installation, configuration, startup, development authentication, test data, service isolation, ports, logs, debugging, targeted checks, and end-to-end QA.

For each blocked check, identify the tool, script, documentation, or access you need. Fix agent instructions that cause setup or verification failures.

Implement useful repository-local improvements. Reuse established tools and commands. Document setup, checks, debugging, and common failures in the appropriate existing documentation or AGENTS.md. Keep instructions short enough to maintain.

Use development credentials and isolated data, and keep secrets out of tracked files and logs. Request the minimum specific external access only when needed; continue other improvements while waiting.

Validate the revised workflow from a clean worktree. Exercise a representative user flow. For a new or changed verification gate, introduce a representative fault in a disposable environment, confirm the gate catches it, and remove the fault.

Provide the working commands, remaining manual steps, and access you still need. Include measured setup or verification times if they help assess the change.
```
