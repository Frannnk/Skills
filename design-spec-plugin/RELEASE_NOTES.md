# Release Notes

## v0.9.0-beta

This release turns the plugin into a publishable beta for enterprise SaaS and admin-console design generation.

### Added

- quick start guide for daily usage
- plugin capability summary
- page-family selection rules
- example-page breakdowns for the supplied admin demo
- high-frequency page rules for dashboard, search-table, analytics, and settings pages
- component composition rules with `Non-negotiable`, `Default`, `Recommended`, and `Avoid` strengths
- state and interaction rules
- component-library mapping and fallback strategy
- lightweight backtest report from realistic page replays

### Improved

- language consistency guidance
- realistic KPI, filter, table, and action generation
- list-page elasticity instead of fixed screenshot copying
- settings-page grouping and action hierarchy
- Figma library generation workflow through explicit screenshot-level QA

### Hardened

- blocking checks for placeholder-copy leakage
- fallback path from composite components to leaf components
- explicit-width-first strategy for first-pass Figma generation
- review flow for mixed-language chrome and unstable library overrides

### Known Limits

- chart-heavy pages still benefit from manual review
- rare library components are less modeled than high-frequency ones
- composite components may still require screenshot-driven cleanup in unusual cases
