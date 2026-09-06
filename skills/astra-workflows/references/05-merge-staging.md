# 5. Review, merge, and verify staging

```text
Review and merge PRs in this explicit scope:
[PR URLs or a precise selection rule]

You may merge qualifying PRs without asking again and deploy the resulting revision to staging through the established workflow. Production deployment is outside this authorization.

Inspect merge policies and deployment triggers first. Confirm that merging will not automatically deploy to production or mutate production data without separate authorization. If it would, complete review and preparation but leave the merge blocked on that boundary.

For each PR, understand the intended result, review the complete diff, resolve material concerns within its scope, and verify affected behavior. Run relevant checks and confirm required CI, approvals, and blocking feedback. Passing CI alone is insufficient evidence of correctness.

Check compatibility, migrations, and rollback limitations where the diff makes them relevant. Use existing staging services and fixtures without destructive shared-data resets.

Use the repository's normal merge method or queue and respect protections and required human approvals. Merge the revision you reviewed and verified. Process dependent PRs in order and revalidate when the base or PR changes.

After merging, verify the resulting revision, its staging deployment, and affected flows. Stop further merges if staging fails and investigate. Execute rollback only where policy or existing authorization permits it; otherwise prepare the specific recovery action.

Report PR links and revisions, checks, and the staging results. Mark pending deployments and blocked PRs as unfinished, with the reason.
```
