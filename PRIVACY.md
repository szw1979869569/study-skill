# Data Privacy and Security Policy

## Purpose

This repository is for research protocols, documentation, reusable code, and approved non-sensitive outputs. It is not an approved storage system for clinical records or restricted research data.

## Never commit

Do not commit, paste into issues, or include in paths, filenames, branch names, commit messages, or logs:

- Direct identifiers or protected health information, including names, medical-record numbers, government identifiers, addresses, contact details, full dates of birth, or identifiable images.
- Raw or identifiable medical records, clinical notes, imaging, laboratory exports, consent forms, linkage files, or recruitment/contact lists.
- Restricted, controlled-access, licensed, data-use-agreement-protected, or institution-only datasets unless written authorization explicitly permits version control here.
- Passwords, API tokens, access keys, private keys, connection strings, cookies, credentials, or secret configuration.
- Row-level data that could enable re-identification, including small cells, rare combinations, precise dates, or granular locations.

These prohibitions apply even if the repository is private. Git history is durable and copied widely.

## Allowed content

Content may be committed only when institutional policy, ethics approval, consent terms, licenses, and data-use agreements permit it. Typical acceptable content includes:

- Protocols, analysis plans, search strategies, empty templates, and data dictionaries without participant values.
- Reusable code using clearly labeled synthetic fixtures or public, non-identifying examples.
- Aggregated results that passed disclosure review and applicable minimum-cell-size rules.
- Metadata and provenance records that do not reveal identities or restricted source data.

Public-use NHANES files should be downloaded from the official source into an ignored local data directory. Do not commit local copies, extracts, or caches unless the project lead explicitly approves a specific non-sensitive artifact.

## Local handling

1. Store raw and restricted data only in an institutionally approved location with appropriate access controls.
2. Use ignored local directories only when local policy permits; `.gitignore` is not a security control.
3. Use environment variables or an approved secrets manager. Commit only safe examples such as `.env.example` with placeholder values.
4. Minimize data and document derivations without reproducing source values.
5. Review tables, figures, reports, logs, and notebook outputs for sensitive content before committing.

## Pre-commit privacy check

Before every commit, confirm that:

- No prohibited data or secrets are present in staged files or filenames.
- Outputs are aggregated, disclosure-reviewed, and permitted for the repository audience.
- Logs, caches, temporary exports, and local configuration are excluded.
- Public datasets are cited by source and version rather than copied unnecessarily.
- The change complies with the protocol, ethics approval, license, and data-use agreement.

## Incident response

If sensitive data or a secret is committed:

1. Stop pushing, sharing, or cloning and notify the project lead and institutional privacy/security contact immediately.
2. Revoke and rotate exposed credentials.
3. Follow institutional incident-response requirements and document the event outside this repository.
4. Remove the material from the current tree and Git history using an approved process; deleting only the latest file is insufficient.
5. Assess clones, forks, caches, releases, and CI artifacts before restoring normal access.

When uncertain, do not commit the file. Ask the project lead or data steward first.
