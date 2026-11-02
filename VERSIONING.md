# Versioning and File Naming

## Repository versions

Use semantic versions (`MAJOR.MINOR.PATCH`) for reviewed repository releases:

- **MAJOR:** incompatible governance or workspace changes.
- **MINOR:** new research areas, templates, or backward-compatible workflows.
- **PATCH:** clarifications and backward-compatible fixes.

Record notable changes in `CHANGELOG.md`. Use Git tags only after review and approval.

## Document versions

Every protocol and formal result record should include a version, date, owner, status, and approval reference. Start drafts at `0.1`; use `1.0` for the first approved version. Record amendments rather than silently replacing decisions.

## Naming conventions

Use lowercase ASCII kebab-case for folders and filenames, for example:

```text
gc-survival-2026/
protocol-v1.0.md
primary-analysis/
result-record-v1.0.md
```

Use stable project slugs across directories. Never include participant identifiers or sensitive values in names, branches, commits, tags, or issues.

## Analysis traceability

A result record should identify the protocol version, analysis ID, source-data version or access date, data-dictionary version, code commit SHA, software environment, and review status. Do not encode restricted data values in Git metadata.
