# Install Guide

This guide explains how to use `design-spec-plugin` as a local Codex plugin.

## Requirements

- Codex desktop or a Codex environment that supports local plugins
- Access to this repository on your local machine

## Plugin Location

The plugin lives at:

```text
design-spec-plugin/
```

Its plugin manifest is:

```text
design-spec-plugin/.codex-plugin/plugin.json
```

## Recommended Local Setup

1. Clone or download this repository locally.
2. Keep the repository in a stable workspace path.
3. Point your Codex local plugin setup at:

```text
design-spec-plugin
```

## What To Open First

If this is your first time using the plugin, start with:

- `design-spec-plugin/README.md`
- `design-spec-plugin/QUICK_START.md`
- `design-spec-plugin/PLUGIN_CAPABILITIES.md`

If you want the full rule layer, open:

- `design-spec-plugin/skills/design-spec-enforcer/SKILL.md`

## Typical Use

Once the plugin is available to Codex, ask for design work in plain language, for example:

```md
Design a user management homepage with KPI cards, filters, a table, and batch actions.
```

Or in Chinese:

```md
按我的 SaaS design spec，设计一个用户管理后台首页，要有概览卡片、筛选、表格和批量操作。
```

## Best Results

For more stable output, include:

- page type
- page goal
- target users
- core modules
- primary actions
- language mode
- required states
- special constraints

## Troubleshooting

### The plugin is installed but output feels too generic

Open and refine:

- `design-spec-plugin/skills/design-spec-enforcer/DESIGN_SPEC.md`
- `design-spec-plugin/skills/design-spec-enforcer/PAGE_PATTERNS.md`

### Figma output still shows placeholder copy

Check:

- `design-spec-plugin/skills/design-spec-enforcer/LANGUAGE_QA_RULES.md`
- `design-spec-plugin/skills/design-spec-enforcer/COMPONENT_LIBRARY_MAPPING.md`

### The page family feels wrong

Check:

- `design-spec-plugin/skills/design-spec-enforcer/PAGE_SELECTION_RULES.md`
- `design-spec-plugin/skills/design-spec-enforcer/EXAMPLE_PAGE_INDEX.md`

## Notes

- This repository is structured for local plugin usage first.
- Metadata URLs inside the plugin manifest currently use placeholder website links and can be replaced later.
