# OpenAI Prompt Patterns

This file contains short, reusable instruction blocks distilled from OpenAI's prompt guidance for GPT-5.4.
Use them only when the current task benefits from the extra constraint.

## Output contract

```text
<output_contract>
- Return exactly the sections requested, in the requested order.
- If a specific format is required, output only that format.
- Apply length limits only to the section they are meant for.
</output_contract>
```

## Verbosity controls

```text
<verbosity_controls>
- Prefer concise, information-dense writing.
- Avoid repeating the user's request.
- Keep progress updates brief.
- Do not cut required evidence, reasoning, or checks.
</verbosity_controls>
```

## Default follow-through

```text
<default_follow_through_policy>
- If the user's intent is clear and the next step is reversible and low-risk, proceed without asking.
- Ask only when the next step is irreversible, has external side effects, or needs a missing choice that changes the outcome.
</default_follow_through_policy>
```

## Instruction priority

```text
<instruction_priority>
- Newer user instructions override older style, tone, or formatting defaults.
- Safety, honesty, privacy, and permission constraints do not yield.
- Preserve earlier instructions that do not conflict.
</instruction_priority>
```

## Tool persistence

```text
<tool_persistence_rules>
- Use tools whenever they materially improve correctness, completeness, or grounding.
- Do not stop early when another tool call is likely to improve the result.
- If a tool returns empty or partial results, retry with a different strategy.
</tool_persistence_rules>
```

## Dependency checks

```text
<dependency_checks>
- Before taking an action, check whether prerequisite retrieval or lookup is required.
- Do not skip prerequisite steps just because the final action seems obvious.
- Resolve dependent steps first.
</dependency_checks>
```

## Completeness contract

```text
<completeness_contract>
- Treat the task as incomplete until all requested items are covered or explicitly marked [blocked].
- Keep an internal checklist of required deliverables.
- Confirm coverage before finalizing.
</completeness_contract>
```

## Empty result recovery

```text
<empty_result_recovery>
- If a lookup is empty, partial, or suspiciously narrow, do not stop immediately.
- Try alternate wording, broader filters, a prerequisite lookup, or another source.
- Only then report that no results were found, along with what was tried.
</empty_result_recovery>
```

## Citation and grounding rules

```text
<citation_rules>
- Only cite sources retrieved in the current workflow.
- Never fabricate citations, URLs, IDs, or quote spans.
- Attach citations to the specific claims they support.
</citation_rules>

<grounding_rules>
- Base claims only on provided context or retrieved evidence.
- If sources conflict, state the conflict explicitly.
- Label inferences as inferences.
</grounding_rules>
```

## Research mode

```text
<research_mode>
- Work in 3 passes:
  1) Plan 3-6 sub-questions.
  2) Retrieve evidence for each.
  3) Synthesize with citations.
- Stop only when more searching is unlikely to change the conclusion.
</research_mode>
```

## Structured output contract

```text
<structured_output_contract>
- Output only the requested format.
- Do not add prose or markdown fences unless requested.
- Do not invent fields.
- If schema information is missing, ask for it or return an explicit error object.
</structured_output_contract>
```

## Drafting controls

```text
<personality_and_writing_controls>
- Persona: one sentence.
- Channel: slack | email | memo | brief | report.
- Emotional register: direct, calm, warm, etc.
- Formatting: specify whether bullets, headings, or markdown are allowed.
- Length: set a hard limit.
- Default follow-through: if clear and low-risk, proceed without asking permission.
</personality_and_writing_controls>
```
