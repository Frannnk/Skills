# SaaS List Layout Rules

Use this file for all list-heavy pages. The goal is to classify list pages by structure and interaction density, then generate a layout that scales instead of hardcoding one screenshot-like arrangement.

## 1. Core Principle

- Do not treat any reference page as a frozen template.
- Learn the page family, block order, density, and interaction model from the reference.
- Keep the layout elastic enough to support different record types, different filter counts, and different action densities.
- A page that needs 3 rows of filters must still feel intentional, not like a broken 2-row design.

## 2. List Page Families

### Search Table

- Best for: structured records, operations, permissions, tickets, users, orders, assets
- Primary result surface: table
- Typical block order:
  - breadcrumb and title
  - optional KPI or summary cards
  - search and filter area
  - toolbar
  - table
  - pagination
- Typical behavior:
  - quick search plus multiple attribute filters
  - bulk actions after selection
  - row actions and status chips inside the table

### Card List

- Best for: entities that need richer previews, media, multi-line summaries, ownership, progress
- Primary result surface: repeatable cards
- Typical block order:
  - page context
  - filter and sort area
  - optional tabs or view switcher
  - card grid or card list
  - pagination or incremental load
- Typical behavior:
  - sort, filter, quick actions, and lightweight item operations

### Hybrid List

- Best for: pages that switch between table and card result views, or combine KPI summaries with a dense operational result set
- Primary result surface: table and cards are both valid
- Typical block order:
  - page context
  - overview or tabs
  - filter area
  - toolbar with view controls
  - active result surface
- Typical behavior:
  - supports multiple presentation modes without changing information architecture

### Directory / Hierarchical List

- Best for: org structures, file systems, category trees, policy groups
- Primary result surface: tree, split view, or nested table
- Typical block order:
  - context
  - scope filters
  - left tree or category rail
  - right detail list or detail panel
- Typical behavior:
  - hierarchy navigation is first-class
  - local filters refine the current branch, not the whole system

## 3. Filter Architecture

Do not think in terms of fixed “one-row filters” or “two-row filters”. Think in terms of filter priority and packing rules.

### Filter Tiers

- Tier A: must-visible controls
  - keyword search
  - primary status filter
  - one or two business-critical dimensions
- Tier B: useful but not always required
  - role, owner, source, organization, time range, region
- Tier C: advanced or low-frequency controls
  - long-tail attributes
  - rarely used flags
  - secondary ranges and niche dimensions

### Placement Rules

- Always show Tier A by default.
- Show Tier B inline when the available width supports it cleanly.
- Move Tier C into:
  - a second or third filter row when the page is filter-heavy and operators need constant visibility
  - or an expandable “More Filters” area when the controls are lower frequency
- Do not hide critical operational filters behind “More Filters”.

## 4. Elastic Filter Row Rules

### Row Capacity Logic

- Determine row count from available width, control priority, and minimum control width.
- Never decide row count from the reference screenshot alone.
- Desktop list pages should usually target:
  - 1 row for light filtering
  - 2 rows for common operational filtering
  - 3 rows when the workflow genuinely requires more dimensions
- More than 3 visible rows should trigger a layout review:
  - move low-priority controls into expandable filters
  - merge related fields
  - switch some filters to tabs or segmented scopes
  - split the workflow into a higher-level scope selector plus local filters

### Minimum Control Widths

- keyword search: `220px` to `320px`
- standard select/date field: `160px` to `220px`
- compact enum or status select: `140px` to `180px`
- action buttons on the filter block: size to content, but keep the block visually stable

### Wrapping Rules

- Keep the first row visually strongest.
- Rows should wrap by control groups, not by accidental orphan fields.
- Keep search first unless the domain strongly needs a scope selector first.
- Keep primary submit and reset actions aligned with the filter system, not floating far away.
- If a row wraps, preserve consistent vertical rhythm between rows, usually `12px` to `16px`.

## 5. Filter Block Composition

### Recommended Patterns

- Pattern A: inline search form
  - use when filters are light and the page is highly repetitive
- Pattern B: multi-row search form
  - use when operators need several dimensions visible at all times
- Pattern C: compact top row plus expandable advanced filters
  - use when the domain has many possible filters but only a few are used every day
- Pattern D: tabs plus local filters
  - use when one top-level category heavily changes the meaning of the result set

### Interaction Rules

- Search or query action should be primary.
- Reset should be secondary and close to search.
- “More Filters” should be tertiary.
- Export, density, column settings, and refresh belong in the toolbar, not the filter form.

## 6. Table Toolbar Rules

Separate toolbar behavior from filter behavior.

### Left Side

- selection count
- bulk actions
- context-sensitive operations that only appear after selection

### Right Side

- column settings
- refresh
- density switch
- export
- view switcher when relevant

### Rules

- Bulk actions should not visually compete with the page-level primary CTA.
- Right-side utility actions should be lighter than the main CTA.
- Do not mix row-level actions into the table toolbar.

## 7. Result Surface Rules

### Table

- Use for precision tasks, auditability, comparisons, and batch operations.
- Keep row height compact but readable.
- Use status chips, concise secondary text, and predictable action placement.

### Cards

- Use when each entity needs a richer summary or visual context.
- Keep the card skeleton consistent across items.
- Put shared metadata in stable zones to support scanning.

### View Switching

- If the same data needs table and card views, keep:
  - identical filter logic
  - identical sorting semantics
  - consistent item identity fields
- Only the result surface should change, not the page meaning.

## 8. Adaptation Heuristics

When the requested content exceeds the reference density:

- expand to more filter rows before shrinking controls below comfortable widths
- reduce decorative chrome before reducing readability
- keep cards and table containers full-width and calm
- allow the toolbar to wrap only after filters have already been resolved cleanly
- preserve hierarchy: context, filters, toolbar, results

When the requested content is lighter than the reference:

- collapse to a cleaner one-row or one-block filter area
- do not keep empty structural placeholders just to mimic the reference

## 9. Quality Checks

After generating any list page, review:

- whether all visible labels are in the requested language
- whether filter controls wrap intentionally
- whether the first row carries the most important filters
- whether export and utility actions are in the toolbar instead of the filter block
- whether table headers, row actions, and status chips are aligned consistently
- whether the page still works if one more filter field is added
- whether the page still works if a control label becomes longer

## 10. Non-Negotiables

- Do not hardcode the number of filter rows from a reference page.
- Do not force all filters into one row by shrinking controls below readable widths.
- Do not hide critical operational filters only because the screenshot used fewer fields.
- Do not mix page CTA, search CTA, utility actions, and bulk actions into one undifferentiated button cluster.
