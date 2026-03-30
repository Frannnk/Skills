# Plugin Capabilities

This file explains what the SaaS Design Spec Plugin currently does well, what it partially covers, and what still needs human judgment.

## 1. Core Capabilities

### Page family selection

The plugin can classify requests into:

- workplace dashboard
- monitor dashboard
- analytics page
- search table page
- card list page
- grouped form
- step form
- profile or settings page
- result or exception page

### Example-driven structure

The plugin can map requests to example routes and borrow:

- block order
- section rhythm
- module mix
- action hierarchy

### List-page layout logic

The plugin can:

- decide filter density
- separate filters from toolbar utilities
- distinguish page CTA from bulk and utility actions
- keep list pages elastic instead of freezing one screenshot

### Content realism

The plugin can:

- avoid generic demo wording
- suggest realistic KPIs
- choose plausible statuses and actions
- keep page modules inside one coherent business domain

### Language and QA

The plugin can:

- keep Chinese and English chrome consistent
- detect likely placeholder leakage
- enforce a review checklist before presentation

### Component-library guidance

The plugin can:

- prefer high-frequency library components
- suggest likely component families and override points
- decide when primitives are still acceptable

## 2. Strongest Use Cases

- user management
- customer ticket management
- order management
- operational dashboards
- account settings
- analytics pages with KPI and trend structure

## 3. Partial Capabilities

These areas are covered, but still benefit from hands-on review:

- complex chart storytelling
- multi-level navigation systems
- rare or niche components
- deeply customized workflow pages
- heavily localized bilingual enterprise products

## 4. What The Plugin Does Not Guarantee

- pixel-perfect reproduction of every example page
- full coverage of every component variant in the library
- automatic extraction of every hidden rule from the reference system
- perfect behavior without prompt quality

## 5. Best Practices For Users

- say the page type clearly
- say the main task clearly
- say the target users clearly
- say whether KPI cards are needed
- specify language mode if it matters
- specify if the result surface must be table, card, or hybrid
- mention any structural override early

## 6. Release Status

Current practical status:

- usable for real internal design generation
- suitable for beta release
- still benefits from real-page backtesting and refinement
