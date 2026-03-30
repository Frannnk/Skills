# SaaS Language And QA Rules

Use this file to keep generated designs consistent in language, labels, and post-generation quality checks.

## 1. Language Mode

Every generated page should assume one of these modes:

- `zh-CN`
- `en-US`
- `bilingual`

If the user does not specify a mode:

- default to `zh-CN` when the request is in Chinese
- default to `en-US` when the request is in English

## 2. Language Consistency Rules

- Do not mix Chinese and English in the same page chrome unless the page is explicitly bilingual.
- Chrome includes:
  - page title
  - breadcrumb
  - filter labels
  - button text
  - toolbar actions
  - table headers
  - status labels
  - empty states
  - helper text
- Product names, emails, and proper nouns may stay in their original form.
- Data values may remain numeric or internationally formatted as needed.

## 3. Allowed Exceptions

Mixing is allowed only when one of these is true:

- the user explicitly asks for bilingual output
- the page is for international or language-learning operations
- a legal or product term should stay in English
- code-like identifiers, SKUs, IDs, and email addresses are shown

## 4. Placeholder Replacement Rules

Never leave library-default placeholder copy visible in the final result unless the user requested a generic demo.

High-risk leftovers include:

- `Menu Item 1`
- `Primary Action`
- `More`
- `All statuses`
- `All roles`
- `Select an option`
- `Search`
- `Sample Product`
- `No data`

Before finalizing a page:

- replace generic navigation labels
- replace generic statistic titles
- replace generic button text
- replace generic status/filter placeholders
- replace default table cell demo text

For library-driven Figma output:

- do not trust instance creation success as proof that text overrides applied visually
- always run a screenshot check after generation
- treat visible library-default copy as blocking, even if the underlying component properties were edited
- if a composite instance keeps placeholder copy, fall back in this order:
  - exposed component property
  - safe-font override on the visible text node
  - leaf-level component instead of the aggregated component
  - primitive wrapper around smaller library instances

## 5. Date And Number Rules

For `zh-CN`:

- prefer Chinese labels
- keep date ordering stable and readable
- use short operational formats in dense tables

For `en-US`:

- keep the whole chrome in English
- keep date and label casing consistent

For bilingual:

- define one dominant language and one supporting language
- do not alternate languages randomly across sibling controls

## 6. Post-Generation QA Checklist

After generating a page, always review:

- whether the page family matches the requested task
- whether the selected language mode is consistent
- whether any default library copy remains visible
- whether composite components still show untouched internal labels
- whether filter rows wrap intentionally
- whether filter actions are separate from toolbar utilities
- whether page CTA, bulk actions, and utility actions are clearly separated
- whether labels are truncated or crowded
- whether one additional filter would still fit cleanly
- whether a longer translated label would still fit cleanly

## 7. Auto-Fix Priorities

If issues are found, fix in this order:

1. wrong page family
2. mixed-language chrome
3. placeholder or library-default copy leakage
4. failed composite-component text replacement
5. broken filter wrapping
6. crowded toolbar or action hierarchy
7. visual polish issues

## 8. Review Output Format

When reviewing or self-checking, categorize issues as:

- language consistency
- layout elasticity
- action hierarchy
- component consistency
- content realism

This keeps later correction passes focused.
