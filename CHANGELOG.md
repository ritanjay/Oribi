# Changelog

All notable changes to Oribi are recorded here.

## Unreleased

- Make shareable exports omit sampled cell values by default; add explicit `include_values` opt-in and safe top-frequency counts. Serialized schema version is now `2`.
- Separate observed unique keys from approximate candidates, and prevent colliding or null-bearing candidates from establishing grain.
- Distinguish exact dependencies from approximate mappings with contradiction and paired-row evidence; exclude numeric measures from entity grouping inference.
- Bound relationship discovery, compact-context rendering, and temporal gap examples; retain schema information on wide frames.
- Profile meaningful pandas indexes separately from columns and reduce identifier confidence for highly repeated low-diversity codes.
- Count index duplicates with `Index.duplicated()`, so a single missing index entry is no longer reported as a duplicate of a unique index; repeated missing entries still count (#43).
- Print each warning message once in `to_markdown()`: a column lists its warnings by severity and title and points to "Analytical warnings", which keeps the full message, implication and suggestion (#44).
- Detect mixed-type object columns from every non-missing value instead of the first 100, so the logical type no longer depends on row order (#5).

## 0.1.0 — Initial release

- Introduce the `oribi` pandas DataFrame profiling API.
- Report column statistics, evidence-backed semantic roles, recommendations, warnings, relationships, candidate keys, and likely grain.
- Add conservative temporal-gap warnings for regular datetime series.
- Provide summary, dictionary, JSON, Markdown, and bounded AI-oriented context output.
