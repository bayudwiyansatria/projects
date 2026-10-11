# Projects

[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-ff69b4.svg)](CODE_OF_CONDUCT.md)

A reusable repository template for development and operations projects. It provides collaboration files, repository
hygiene, documentation examples, and a minimal automation baseline without choosing an application stack.

## Included baseline

| Area               | Included                                                                      |
| ------------------ | ----------------------------------------------------------------------------- |
| Collaboration      | Contribution, conduct, support, security, issue, and pull-request guidance    |
| Ownership          | A starter `CODEOWNERS` file that must be reviewed for each repository         |
| Automation         | Feature and default-branch secret-detection workflows                         |
| Maintenance        | GitHub Actions dependency updates and release-drafter configuration           |
| Repository hygiene | EditorConfig, Git attributes, common ignore rules, MIT license, and changelog |
| Documentation      | Template guidance plus change-log and release-note examples                   |
| Agent guidance     | A root `AGENTS.md` describing how to maintain and adapt the template          |

The template deliberately contains no language manifest, application source, build, test, publication, or deployment
job. Add those only after selecting the project runtime and delivery model.

## Use this template

Select **Use this template** on GitHub, or use the GitHub CLI:

```shell
gh repo create OWNER/REPOSITORY \
  --template bayudwiyansatria/projects \
  --clone
```

Choose the target repository's owner and visibility when prompted. A generated repository has independent history and
does not automatically receive later changes from this template. The included workflow triggers use `main` as the
default branch.

## Adapt the generated repository

Before product work begins:

1. Rewrite `README.md` with the project's purpose, architecture, requirements, setup, commands, configuration, and
   ownership.
2. Rewrite `AGENTS.md` with verified module boundaries, working rules, and validation commands.
3. Review `CODEOWNERS`, contribution guidance, support and security contacts, license, notice, and repository metadata.
4. Select the runtime and commit its manifests and lockfiles. Review `.gitignore` before adding patterns so broader or
   duplicate rules are not introduced.
5. Use `main` as the default branch, or update every workflow trigger that names it.
6. Extend the workflows with build and test jobs appropriate to the selected stack. Add release or deployment jobs only
   after their artifacts, credentials, environments, and promotion behavior are defined.
7. Add each committed package ecosystem to `.github/dependabot.yml`.
8. Copy and rename the examples under `docs/changes-log/` and `docs/release-notes/`; do not edit the `.example` files as
   if they were project history.
9. Review branch protection, required checks, Actions permissions, environments, variables, and secrets.

See the [repository template guide](docs/README.md) for the design boundaries and a more detailed adoption checklist.

## Repository structure

```text
.github/              ownership, issue and pull-request templates, automation, and dependency updates
docs/                 template guide and documentation examples
AGENTS.md              instructions for agents working in this repository
CHANGELOG.md           history of this repository
CODE_OF_CONDUCT.md     community standards
CONTRIBUTING.md        contribution workflow
SECURITY.md            vulnerability reporting and supported-version policy
SUPPORT.md             support channels and scope
```

## Validation

This repository has no application build. Before proposing a template change, run:

```shell
git diff --check
git status --short
```

Also parse changed YAML, verify changed relative Markdown links, and review workflow permissions and branch filters.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Report security issues through the process in [SECURITY.md](SECURITY.md), not a
public issue.

## Author

[Bayu Dwiyan Satria](https://github.com/bayudwiyansatria)

## License

Licensed under the [MIT License](LICENSE).
