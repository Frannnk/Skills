# Skills Repository

This repository contains reusable Codex skills and plugins for product design generation workflows.

## Included

### `design-spec-plugin`

A local Codex plugin for generating stable SaaS and admin-console interfaces from a structured design specification.

What it includes:

- page-family selection rules
- list-page layout rules
- component composition rules
- state and interaction rules
- language QA rules
- component-library mapping guidance
- prompt templates and brief templates
- backtest notes and release notes

## Repository Structure

```text
.
├── design-spec-plugin/
│   ├── .codex-plugin/
│   ├── skills/
│   ├── assets/
│   ├── examples/
│   └── README.md
├── LICENSE
└── README.md
```

## Quick Use

If you are using Codex locally, point it at `design-spec-plugin` as a local plugin.

Useful entry files:

- `INSTALL.md`
- `design-spec-plugin/README.md`
- `design-spec-plugin/QUICK_START.md`
- `design-spec-plugin/PLUGIN_CAPABILITIES.md`
- `design-spec-plugin/skills/design-spec-enforcer/SKILL.md`

## Notes

- The plugin is packaged as a local Codex plugin.
- Metadata for homepage and repository currently uses placeholder URLs and can be replaced later with the final public links.
- The plugin content is written as a neutral SaaS design system package and does not expose source-system branding in the public-facing rules.
