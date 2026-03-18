# Contributing to the Red Team Testing Guide

Thank you for your interest in improving this guide. Contributions from security researchers, AI engineers, and red team practitioners help keep this resource current and comprehensive.

## How to Contribute

### Reporting Issues

- **Error in existing scenario:** Open an issue using the [Bug Report template](.github/ISSUE_TEMPLATE/bug_report.md)
- **New scenario proposal:** Open an issue using the [New Scenario template](.github/ISSUE_TEMPLATE/new_scenario.md)
- **Regulatory update:** Open an issue describing the regulatory change and which scenarios it affects

### Submitting Changes

1. Fork this repository
2. Create a branch: `git checkout -b your-category/description`
3. Make your changes following the guidelines below
4. Submit a pull request using the [PR template](.github/PULL_REQUEST_TEMPLATE.md)

## Scenario Format

Every test scenario must follow this structure:

```markdown
### Q[N]. [Scenario Name]

**Threat:** [Category] – [Subcategory]

**Scenario:** [Clear description of the attack]

**Variations:**
- [Variation 1]
- [Variation 2]

**Expected Safe Response:**

> "[The ideal response the system should give]"

**Mitigation:** [Concrete defensive measures]
```

A blank template is available at [templates/scenario-template.md](templates/scenario-template.md).

## Q Numbering

- New scenarios extend from Q163+
- Never renumber existing scenarios — this breaks cross-references in organizations already using the guide
- If adding scenarios to an existing category, append them at the end of that category's file

## File Naming

- Category files: `NN-kebab-case.md` (e.g., `24-new-category.md`)
- Keep filenames lowercase with hyphens, no spaces
- Section numbers are sequential across the entire guide

## Content Guidelines

- **Be specific.** Vague scenarios like "try to trick the AI" aren't useful. Provide exact prompts and expected behaviors.
- **Include variations.** At least 2 variations per scenario help testers explore the attack surface.
- **Actionable mitigations.** "Be more secure" isn't a mitigation. "Implement per-action confirmation for state-changing operations" is.
- **Plain language.** This guide is used by security teams, product managers, and compliance officers — not just ML researchers.
- **Include regulatory mapping.** When adding new categories, map them to OWASP LLM Top 10, EU AI Act articles, and MITRE ATLAS where applicable.

## System Prompt Examples

If adding a new category, include a System Prompt Protection Example showing how defenders can mitigate the attack class. Also add it to [docs/system-prompts.md](docs/system-prompts.md).

## What We're Looking For

Priority areas for contribution:
- New attack techniques discovered in the wild
- Scenarios for emerging AI capabilities (e.g., new tool protocols, new modalities)
- Regulatory updates (new AI legislation, updated standards)
- Improved mitigations based on real-world deployment experience
- Translations of the guide

## Code of Conduct

- This guide is for **defensive security** — helping organizations protect their AI systems
- Do not include working exploits, malware, or attack tooling
- Do not submit scenarios that target specific commercial products by name
- Be respectful in issues and pull requests

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](LICENSE).
