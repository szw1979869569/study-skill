# Analysis Scripts

Store reproducible source code and safe configuration examples here. Create one folder per analysis, copy `analysis-readme-template.md`, and organize scripts in execution order when practical (for example, `01-prepare`, `02-analyze`, `03-report`).

## Minimum standards

- Read data from ignored local paths or approved secure storage; never hard-code credentials or identifiers.
- Keep source data immutable and write derived data to ignored locations.
- Set and record random seeds when relevant.
- Capture package/software versions and all non-sensitive parameters.
- Validate cohort flow, uniqueness, ranges, missingness, joins, and model assumptions.
- Generate results into ignored staging locations and commit only disclosure-safe outputs.
- Link every analysis to a protocol version, dictionary, and result record.
