# 15 Astra prompts for real projects

![Black-and-white editorial cover: 15 prompts for real projects](assets/cover.png)

Copy a prompt or install the **Astra Workflows** skill for Codex or Claude Code. Choose a task, define its scope, and give the agent the tools to verify its work.

[Theo shared six ways he uses Astra](https://x.com/theo/status/2095966874010046621): code cleanup, performance work, agent setup, PR and issue triage, merging, and taking over stalled work. I wrote a prompt for each and added nine for tasks such as feature planning, competitor research, and SEO/GEO audits.

[Read the article on X](https://x.com/MaxMalloc/status/2096594162225185218) · [Subscribe to Build notes](https://0xmassi.dev/)

## Copy a prompt

Copy the [shared instructions](skills/astra-workflows/references/shared-instructions.md) and one task below. Each page has a fenced code block with GitHub's copy button. Fill in the bracketed fields and adjust the permissions to your task.

Some copyable prompts authorize remote actions: backlog closures in 4, scoped merges and staging in 5, and draft PRs in 6 and 12. Read that scope before sending a prompt. Append the [report-only modifier](skills/astra-workflows/references/modifiers.md) for an observational audit.

| # | Task | Result |
|---|---|---|
| 1 | [Slop audit and cleanup](skills/astra-workflows/references/01-slop-cleanup.md) | Remove unnecessary complexity while preserving behavior |
| 2 | [Measurable performance wins](skills/astra-workflows/references/02-performance.md) | Compare a reproducible baseline with the change |
| 3 | [Agent setup and verification](skills/astra-workflows/references/03-agent-setup.md) | Make setup, debugging, and QA usable from a fresh checkout |
| 4 | [PR and issue triage](skills/astra-workflows/references/04-backlog.md) | Assess open work and close items with supporting evidence |
| 5 | [Review, merge, and verify staging](skills/astra-workflows/references/05-merge-staging.md) | Review specified PRs and verify the authorized staging release |
| 6 | [Take over stalled work](skills/astra-workflows/references/06-takeover.md) | Repair, simplify, or restart work to meet its requirements |
| 7 | [Bug hunt](skills/astra-workflows/references/07-bug-hunt.md) | Reproduce failures and fix root causes |
| 8 | [Security review](skills/astra-workflows/references/08-security.md) | Confirm vulnerabilities and verify scoped fixes |
| 9 | [CI and test reliability](skills/astra-workflows/references/09-ci-reliability.md) | Fix unreliable checks without weakening coverage |
| 10 | [User journey QA](skills/astra-workflows/references/10-user-journey-qa.md) | Exercise the app and repair confirmed failures |
| 11 | [Dependency maintenance](skills/astra-workflows/references/11-dependencies.md) | Resolve concrete security, support, or compatibility problems |
| 12 | [Feature or project implementation](skills/astra-workflows/references/12-implement.md) | Deliver the accepted scope and verify its behavior |
| 13 | [Feature or project planning](skills/astra-workflows/references/13-plan.md) | Produce a plan and a copyable implementation handoff |
| 14 | [Competitor and customer research](skills/astra-workflows/references/14-competitor-research.md) | Investigate pain points and rank product opportunities |
| 15 | [SEO/GEO website audit](skills/astra-workflows/references/15-seo-geo.md) | Inspect pages and document verified blockers and opportunities |

[Optional modifiers](skills/astra-workflows/references/modifiers.md): report only, deliver a draft PR, independent review, and resume interrupted work.

## Install the skill

The skill reads the shared instructions and the workflow you select. It uses the same files linked above. You do not need to paste the pack into each session.

Clone this repository into a new folder:

```sh
git clone https://github.com/0xMassi/astra-prompts.git
cd astra-prompts
```

Run the command for your agent from the cloned repository. These commands stop if a folder or symlink named `astra-workflows` exists at the destination.

**Codex**

```sh
mkdir -p "$HOME/.agents/skills"
if [ -e "$HOME/.agents/skills/astra-workflows" ] || [ -L "$HOME/.agents/skills/astra-workflows" ]; then
  echo "astra-workflows already exists; inspect it before updating."
else
  cp -R skills/astra-workflows "$HOME/.agents/skills/astra-workflows"
fi
```

```text
Use $astra-workflows plan to create an implementation plan for [idea]. Save the plan; do not implement it yet.
```

**Claude Code**

```sh
mkdir -p "$HOME/.claude/skills"
if [ -e "$HOME/.claude/skills/astra-workflows" ] || [ -L "$HOME/.claude/skills/astra-workflows" ]; then
  echo "astra-workflows already exists; inspect it before updating."
else
  cp -R skills/astra-workflows "$HOME/.claude/skills/astra-workflows"
fi
```

```text
/astra-workflows plan an implementation for [idea]. Save the plan; do not implement it yet.
```

For a project-scoped install, copy the entire `astra-workflows` folder into that project's `.agents/skills/` for Codex or `.claude/skills/` for Claude Code. For other agents that support `SKILL.md`, use their documented skill location and invocation syntax. Keep the `references` folder with `SKILL.md`.

Installation and invocation follow the [Codex skill documentation](https://learn.chatgpt.com/docs/build-skills) and [Claude Code skill documentation](https://code.claude.com/docs/en/skills). The skill does not switch models, connect services, or change your agent's tool permissions.

## Choose a session and scope

Start a new session for a new objective. Keep a feature and its debugging together. Give parallel tasks separate branches or worktrees and clear ownership of the files they change. Check the combined result before merging.

Start with **3** if the agent cannot run or test the app. For product work, use **14** to research an opportunity, **13** to plan it, and **12** to implement the accepted plan. Use **15** to audit the website. Each transition requires a request for the next task.

When using the installed skill, your request and existing conversation determine permissions. The template's example grants do not authorize actions on their own. An audit stays observational unless you request fixes; closing PRs, merging, and deploying require authorization for those actions.

Adapt shared rules for your project's `AGENTS.md` or `CLAUDE.md`. Keep task procedures in the skill so you load them when needed.

## Optional tooling

The workflows follow the repository's existing language and toolchain. [Bun 1.4.1, Ponytail, and Stop Slop](TOOLING.md) are personal choices described in the article. You can use the pack without them.

## Reuse

The prompts and skill are available under the [MIT license](LICENSE). Copy, adapt, and share them with the license notice.

## Build notes

I write about building software in [Build notes at 0xmassi.dev](https://0xmassi.dev/). Subscribe for more.
