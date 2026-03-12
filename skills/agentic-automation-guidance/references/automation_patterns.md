# Automation patterns

## What this skill is
A guidance layer for multi-step, tool-using workflows where the assistant should keep going until the task is completed or explicitly blocked.

## How to use it
Activate it for requests like:
- "run this multi-step process"
- "use the available tools and finish the workflow"
- "check dependencies and complete what you can"
- "automate this recurring operational task"

## Default run report

### Goal
What the workflow was meant to achieve.

### Outcome
Completed / partially completed / blocked.

### Actions taken
- step completed
- step completed
- step completed

### Verification
What checks were performed before finishing.

### Blocker or next step
What still prevents full completion, if anything.

## Workflow checklist
- Were prerequisites resolved first?
- Were independent retrieval steps parallelized selectively?
- Were risky actions held for confirmation?
- Was completion verified before closing?
