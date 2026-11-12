---
name: review-diff
description: Review a Git diff for actionable correctness, security and regression issues.
---

1. Identify the requested diff or base ref. If neither is given, inspect staged and unstaged changes and report which scope was reviewed.
2. Read relevant callers, tests and prior behavior. Focus on bugs introduced by the change and look for concrete triggering inputs.
3. Report findings by severity. For each one, include the affected file and line, the trigger, and the observable impact.
4. Separate verified findings from remaining validation gaps. If there are no actionable findings, say so. Keep the repository read-only during the review.
