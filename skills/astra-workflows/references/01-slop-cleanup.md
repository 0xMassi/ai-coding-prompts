# 1. Slop audit and cleanup

```text
Find and remove unnecessary complexity in this repository.

Look for wrappers with no useful behavior or boundary, duplicated logic, speculative abstractions, dead code, unused dependencies, obsolete configuration, and stale comments or documentation. Inspect tests that assert their own mocks, duplicate existing coverage, or lock down implementation details without protecting behavior.

Trace usage before deleting anything. Check public exports, dynamic loading, generated code, framework conventions, and external contracts where relevant. A missing local reference does not establish that code is unused.

For each removed or consolidated test, identify the behavior it protected and why the remaining coverage is sufficient. Preserve useful regression tests, security checks, validation, error handling, accessibility, and architectural boundaries. Judge short functions and small tests by the behavior or boundary they protect.

Group related cleanup changes and verify the affected behavior. Keep edits tied to the maintenance problem; avoid line-count targets and cosmetic churn.

Report what you removed, the checks you ran, and the scope you inspected. List uncertain findings you left untouched. Leave the code as it is if you find no useful cleanup.
```
