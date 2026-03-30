# SaaS Design Spec Plugin

This plugin gives Codex a local, reusable spec for generating enterprise SaaS interfaces with a stable, systemized product design language.

## What is included

- `skills/design-spec-enforcer/DESIGN_SPEC.md`
  A concrete design spec distilled from the provided design system library, official design guidance, theme tokens, and SaaS demo structure.
- `skills/design-spec-enforcer/PAGE_PATTERNS.md`
  Reusable page archetypes for workplace dashboards, monitoring views, analytics pages, tables, forms, profiles, settings, and result states.
- `skills/design-spec-enforcer/EXAMPLE_PAGE_INDEX.md`
  A route inventory of the supplied admin demo that maps each sample page into reusable page families.
- `skills/design-spec-enforcer/PAGE_SELECTION_RULES.md`
  Decision rules for choosing the right page family before generation starts.
- `skills/design-spec-enforcer/LANGUAGE_QA_RULES.md`
  Language mode rules, placeholder-copy cleanup, and post-generation QA checks.
- `skills/design-spec-enforcer/COMPONENT_LIBRARY_MAPPING.md`
  High-frequency component families, likely library matches, override notes, and fallback strategy for Figma generation.
- `skills/design-spec-enforcer/PROMPT_TEMPLATES.md`
  Ready-to-use prompt templates for generating common SaaS pages and reviewing existing designs.
- `skills/design-spec-enforcer/BRIEF_TEMPLATE.md`
  A compact fill-in template for describing a page request before generation.
- `skills/design-spec-enforcer/PROMPT_TEMPLATES_ZH.md`
  Chinese practical prompt templates for direct day-to-day use.
- `skills/design-spec-enforcer/BRIEF_TEMPLATE_ZH.md`
  Chinese page brief template for fast request drafting.
- `QUICK_START.md`
  Fast onboarding guide for immediate day-to-day use.
- `PLUGIN_CAPABILITIES.md`
  Summary of what the plugin does well, partially, and not yet fully.
- `BACKTEST_REPORT.md`
  Lightweight backtest summary across three realistic page types.
- `RELEASE_NOTES.md`
  Beta release summary and known limits.
- `skills/design-spec-enforcer/RESEARCH_SOURCES.md`
  Neutral research traceability and source-category notes used to shape this plugin.
- `skills/design-spec-enforcer/SKILL.md`
  The workflow Codex should follow before generating or reviewing any UI.

## Recommended workflow

1. Mention this plugin or the `design-spec-enforcer` skill when you want design work.
2. Tell Codex what you want to build:
   - "Create an admin dashboard with my SaaS design spec"
   - "Design a data analysis page in this design-system style"
   - "Review this page against the SaaS design spec"
3. Codex should read the spec, page selection rules, example index, and QA rules first, then compose the page from those constraints.

If you are onboarding a new user, start here:

- `QUICK_START.md`
- `PLUGIN_CAPABILITIES.md`

## Prompt templates

If you want more stable outputs, start from:

- `skills/design-spec-enforcer/PROMPT_TEMPLATES_ZH.md`
- `skills/design-spec-enforcer/BRIEF_TEMPLATE_ZH.md`
- `skills/design-spec-enforcer/PROMPT_TEMPLATES.md`
- `skills/design-spec-enforcer/BRIEF_TEMPLATE.md`

These files are designed to be copied into future requests with minimal edits. If you usually describe work in Chinese, use the `_ZH` versions first.

## If you want to customize the style further

Edit `DESIGN_SPEC.md` first. That file remains the source of truth for future design generations.

If you want to improve page-family matching, edit:

- `skills/design-spec-enforcer/EXAMPLE_PAGE_INDEX.md`
- `skills/design-spec-enforcer/PAGE_SELECTION_RULES.md`

If you want to tighten text consistency or review behavior, edit:

- `skills/design-spec-enforcer/LANGUAGE_QA_RULES.md`

## Notes

- Identity URLs in `.codex-plugin/plugin.json` are still placeholders so you can customize ownership metadata.
- The plugin intentionally focuses on enterprise SaaS and admin-console patterns rather than marketing pages.
