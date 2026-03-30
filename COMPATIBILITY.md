# Compatibility Guide

This repository is packaged first as a **Codex local plugin**, but the rule files can also be reused in other AI tools.

## 1. Can It Be Downloaded And Used Directly?

Yes, but the answer depends on the tool:

- **Codex**
  - yes, directly
  - this is the native target format
- **Claude**
  - not as a Codex plugin
  - use it as a rule pack or project knowledge source
- **Cursor**
  - not as a Codex plugin
  - use it as local documentation, prompt templates, and editor rules input
- **Other AI tools**
  - usually not as a one-click plugin
  - use the markdown files as a portable design-system rule pack

## 2. Codex

This repository supports direct local usage in Codex.

Use:

- `design-spec-plugin/.codex-plugin/plugin.json`

Start with:

- `INSTALL.md`
- `design-spec-plugin/README.md`
- `design-spec-plugin/QUICK_START.md`

## 3. Claude

Claude does not natively install this repository as a Codex plugin.

Recommended usage:

1. download or clone the repository
2. open the rule files as project context
3. use the plugin files as persistent guidance for Claude conversations

Best files to provide Claude:

- `design-spec-plugin/skills/design-spec-enforcer/DESIGN_SPEC.md`
- `design-spec-plugin/skills/design-spec-enforcer/PAGE_PATTERNS.md`
- `design-spec-plugin/skills/design-spec-enforcer/PAGE_SELECTION_RULES.md`
- `design-spec-plugin/skills/design-spec-enforcer/LANGUAGE_QA_RULES.md`
- `design-spec-plugin/skills/design-spec-enforcer/COMPONENT_LIBRARY_MAPPING.md`
- `design-spec-plugin/skills/design-spec-enforcer/PROMPT_TEMPLATES.md`
- `design-spec-plugin/skills/design-spec-enforcer/PROMPT_TEMPLATES_ZH.md`

Practical interpretation:

- in Claude, this works best as a reusable design-rule knowledge base
- not as a native installable plugin format

## 4. Cursor

Cursor also does not natively install this repository as a Codex plugin.

Recommended usage:

1. clone the repository into your workspace
2. keep the plugin markdown files in the repo
3. use the rules and templates as:
   - design documentation
   - prompt context
   - editor rules input

Most useful files in Cursor:

- `design-spec-plugin/README.md`
- `design-spec-plugin/QUICK_START.md`
- `design-spec-plugin/skills/design-spec-enforcer/SKILL.md`
- `design-spec-plugin/skills/design-spec-enforcer/DESIGN_SPEC.md`
- `design-spec-plugin/skills/design-spec-enforcer/PROMPT_TEMPLATES.md`
- `design-spec-plugin/skills/design-spec-enforcer/PROMPT_TEMPLATES_ZH.md`

Practical interpretation:

- in Cursor, this works best as a local design-system rule repository
- not as a native Cursor extension or marketplace plugin

## 5. Portable Usage Pattern

If another tool cannot load Codex plugins directly, treat this repository as a portable package with three layers:

1. **core rules**
   - `DESIGN_SPEC.md`
   - `PAGE_PATTERNS.md`
   - `PAGE_SELECTION_RULES.md`
2. **quality control**
   - `LANGUAGE_QA_RULES.md`
   - `CONTENT_REALISM_RULES.md`
   - `DESIGN_REVIEW_CHECKLIST.md`
3. **ready-to-use prompts**
   - `PROMPT_TEMPLATES.md`
   - `PROMPT_TEMPLATES_ZH.md`
   - `BRIEF_TEMPLATE.md`
   - `BRIEF_TEMPLATE_ZH.md`

## 6. Recommended Wording For Other Tools

If you want to use this repository in Claude, Cursor, or another AI assistant, tell it something like:

```md
Use the markdown files in this repository as the design system source of truth.
Follow the page selection, language QA, component mapping, and prompt template rules before generating UI.
Prefer enterprise SaaS and admin-console patterns instead of generic dashboard layouts.
```

## 7. Bottom Line

- **Direct install:** Codex
- **Download and use as rule pack:** Claude, Cursor, and most other AI tools
- **One-click native plugin outside Codex:** not currently the target format
