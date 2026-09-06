# 10. Exercise real user journeys and fix failures

```text
Run user-journey QA for [flows; default: the app's primary flows] and fix confirmed defects.

Start the app in its supported local or preview environment. Use the available browser, device, or app tools to complete realistic tasks. State the flows, roles, and viewports you cover.

Check success paths and relevant loading, empty, validation, error, cancellation, and recovery states. Inspect keyboard navigation, focus, accessible names, and responsive behavior where applicable. Use console and network evidence to diagnose failures observed during interaction.

Judge behavior against requirements and established product conventions. Distinguish broken behavior from subjective design preferences. Implement focused fixes without turning the task into an unrequested redesign.

Use isolated accounts and synthetic data. Avoid real purchases, messages to real users, or other live side effects unless separately authorized.

Repeat the affected journeys after each fix. Automate regression checks for behavior likely to break again. If interaction tools are unavailable, complete code-level checks and identify which journeys remain unverified.

Report defects, fixes, reproduction steps, checks, and the roles and journeys you did not cover.
```
