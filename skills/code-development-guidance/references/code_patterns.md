# Code patterns

## What this skill is
A guidance layer for coding sessions that pushes the assistant toward inspection, minimal-change implementation, and explicit verification.

## How to use it
Activate it for requests like:
- "debug this error"
- "review this PR"
- "refactor this module"
- "add tests for this behavior"

## Default completion template

### Result summary
One paragraph on the outcome.

### Changes or findings
- root cause / main issue
- implementation detail
- important tradeoff

### Verification
- tests run
- build or lint status
- what could not be verified

### Remaining risk
- edge case
- dependency risk
- follow-up improvement

## Coding checklist
- Was the relevant code inspected before changing it?
- Was the fix scoped tightly?
- Was at least one verification step run?
- Are unverified assumptions stated explicitly?
