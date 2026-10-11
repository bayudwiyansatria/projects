# AGENTS.md

## Scope

This repository is a reusable starting point for development and operations projects. It contains repository settings,
community files, documentation examples, and baseline automation; it does not contain an application runtime or
product architecture. GitHub copies these files into a repository created from the template, and later changes here do
not update existing copies.

## Structure

```text
.github/              ownership, contribution templates, dependency updates, and workflows
docs/                 template guidance plus change-log and release-note examples
AGENTS.md              instructions for agents changing this template
CHANGELOG.md           history of this repository
README.md              template overview and adoption checklist
*.md                   conduct, contribution, security, support, and legal documents
```

## Rules

- Keep defaults reusable. Do not assume the generated repository's language, package manager, framework, deployment
  target, visibility, or release process.
- Check the full target file before copying a rule from a sibling repository. Do not add an exact duplicate, a pattern
  already covered by a broader rule, or stack-specific configuration without a matching need.
- Keep owner-specific references only where the checked-in integration requires them. Adopters must review
  `CODEOWNERS`, contacts, workflow references, branch names, and repository metadata.
- Keep one pull-request template at `.github/PULL_REQUEST_TEMPLATE.md`. Change-log and release-note starter documents
  remain `.example` files under `docs/`; `CHANGELOG.md` records this repository's actual history.
- Do not add build, test, publication, or deployment automation until its runtime and credential contract are known.
- Never commit credentials or private infrastructure details. Preserve unrelated local changes.

## Validation

This repository has no application build. For every change, run:

```bash
git diff --check
git status --short
```

Also parse changed YAML, verify changed relative Markdown links, and review workflow permissions and branch filters.
