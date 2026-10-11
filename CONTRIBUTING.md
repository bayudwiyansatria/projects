# Contributing

Thank you for improving this repository template. By participating, you agree to follow the
[Code of Conduct](CODE_OF_CONDUCT.md).

## Before making a change

Open an issue before a substantial or potentially breaking change. Small documentation and maintenance fixes can go
directly to a pull request.

Evaluate a proposal in two contexts:

1. Does it improve this template repository?
2. Is it a safe default when copied into a new repository with an unknown stack?

Runtime, framework, package, and deployment defaults require a concrete cross-project need. Put specialized defaults in
the appropriate boilerplate repository instead.

## Development

Create a focused branch using `feature/`, `bugfix/`, or `hotfix/`. Keep commits reviewable and avoid mixing unrelated
cleanup with the intended change.

This repository has no application build. Validate changes with:

```shell
git diff --check
git status --short
```

For YAML and workflow changes, also verify the syntax and inspect permissions, triggers, dependencies, inputs, and
secret mappings. Do not treat local review as evidence that a remote workflow completed successfully.

## Pull requests

A pull request should:

- explain the problem and why the proposed default belongs in every generated repository;
- list the validation performed and any checks that could not be run;
- update `README.md`, `AGENTS.md`, or `docs/README.md` when the bootstrap contract changes;
- add an entry under `Unreleased` in `CHANGELOG.md` for a user-visible change;
- avoid credentials, generated output, and unrelated formatting changes; and
- remain compatible with the default `main` branch unless a branch migration is part of the proposal.

At least one owner should review a change before merge. Changes to ownership, security reporting, or workflows deserve
an explicit maintainer review.
