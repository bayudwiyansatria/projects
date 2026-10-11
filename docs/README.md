# Repository template guide

This repository is a stack-neutral source template. GitHub copies every tracked file from the selected template branch
into a new repository with an independent history, so a default must be safe and useful even when the target runtime is
not known.

## Design boundaries

The template owns:

- community-health and contribution files;
- baseline ownership and repository hygiene;
- issue and pull-request intake;
- secret detection on development pull requests, named feature branches, and the default branch; and
- a checklist for selecting project-specific automation.

The template does not own:

- application architecture or source layout;
- a language, runtime, framework, or package manager;
- package, image, or deployment credentials;
- CodeQL languages or build modes;
- version calculation or release artifacts; or
- the generated repository's support and lifecycle policy.

Those decisions must be made in the generated repository and recorded in its README, `AGENTS.md`, workflows, and
project documentation.

## Workflow adoption

The included `features.yml` and `main.yml` are intentionally small. Both call the public organization's reusable secret
detection workflow with read-only repository permissions. Feature pushes and pull requests validate proposed changes;
the default-branch workflow validates merged content.

After choosing a toolchain:

1. Inspect the reusable workflows in `bayudwiyansatria/.github` and confirm their current inputs.
2. Add build and test jobs to Feature and Main using job-level `uses` calls.
3. Make build and test depend on secret detection directly, or through another job that already depends on it.
4. Pass only the credentials required by each job through an explicit `secrets` mapping.
5. Add a Release workflow only after version inputs, artifacts, publication destinations, and promotion behavior are
   defined.
6. Configure CodeQL only after the repository has supported languages and a build strategy.
7. Record successful remote runs separately from configuration review.

## External contribution checklist

Before accepting external contributions, verify:

- README setup instructions work from a clean clone;
- example environment files contain names and safe placeholders, never real values;
- history and tracked files contain no credentials or private infrastructure details;
- private vulnerability reporting or a private security contact is available;
- `CODEOWNERS`, branch protection, required checks, Actions permissions, and environments match actual ownership;
- dependency update entries match every committed package ecosystem;
- workflows from forks cannot access deployment credentials; and
- license, notice, third-party attributions, support policy, and supported versions are accurate.

## Maintaining this template

Review changes as defaults for future repositories. Existing repositories do not inherit template updates, so material
baseline improvements need a separate, deliberate rollout. Preserve stack neutrality here and place specialized starter
code in a purpose-built boilerplate repository.

## Historical records

The template includes two examples:

- [`changes-log/2026-10-11.md.example`](changes-log/2026-10-11.md.example) shows a dated engineering record: what changed,
  why the decisions were made, how the result was checked, and what remains open.
- [`release-notes/1.0.0.md.example`](release-notes/1.0.0.md.example) shows a versioned release record: what shipped,
  compatibility impact, verification, upgrading, known issues, dependencies, and contributors.

Copy an example rather than editing it in place:

```shell
cp docs/changes-log/2026-10-11.md.example docs/changes-log/YYYY-MM-DD.md
cp docs/release-notes/1.0.0.md.example docs/release-notes/MAJOR.MINOR.PATCH.md
```

Replace every example value before committing. Change records and release notes are point-in-time records; do not
rewrite them later to match the current implementation. Update living architecture and guide documents separately.
