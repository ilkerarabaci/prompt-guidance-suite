# Contributing

Thanks for your interest.

## How to contribute

- Open an issue for bugs, installation problems, or unclear behavior
- Open a discussion for new skill ideas or broader design changes
- Submit pull requests for:
  - clearer instructions
  - better trigger descriptions
  - improved example prompts
  - packaging fixes
  - documentation updates

## Contribution guidelines

- Keep `SKILL.md` compact and opinionated
- Put trigger conditions in frontmatter descriptions
- Avoid organization-specific references in public skills
- Prefer concrete examples over long explanations
- Test installability before submitting changes

## Pull request checklist

- Skill name and description are lowercase in YAML frontmatter
- `agents/openai.yaml` includes a clean human-readable display name
- ZIP packaging has the correct root structure
- Example prompts still match the skill's actual behavior
- README and release notes are updated when needed
