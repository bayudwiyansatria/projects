# CHANGELOG

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and published versions follow
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Use [the dated change-record example](docs/changes-log/2026-10-11.md.example) for substantial work sessions and
[the release-note example](docs/release-notes/1.0.0.md.example) for published versions.

## Unreleased

### Added

- Repository-specific agent guidance and template adoption documentation.
- Stack-neutral feature and main workflows that run the shared secret-detection job.
- A single canonical pull-request template and issue-template configuration.
- Reusable dated change-record and versioned release-note examples.

### Changed

- Rewrote the README, contribution, security, and support guidance around the repository-template lifecycle.
- Updated ownership, dependency update, release-drafter, editor, Git, and ignore configuration.
- Updated the Code of Conduct from Contributor Covenant 1.4 to 2.1.

### Removed

- Obsolete Java 7/8 and Node.js 10 workflows, the invalid generic CodeQL workflow, and the legacy stale configuration.
- Duplicate pull-request templates and the misspelled `CHANGLOGS.md` file.
- Project-specific 2019 change and release documents that did not belong in generated repositories.

## 1.0.0 - 2019-11-11

### Added

- Initial development and operations repository template.
