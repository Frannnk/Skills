# SaaS Design Specification

Use this file as the single source of truth when generating enterprise SaaS interfaces in this design-system style.

## 1. Product Context

- Product archetype: enterprise SaaS platform, admin console, operational dashboard, data-heavy back office
- Primary audience: operators, analysts, administrators, business users, internal platform teams
- Primary use cases: overview dashboards, monitoring, data analysis, list management, form workflows, profile/settings, result and exception handling
- Platform focus: desktop-first web application
- Product promise: efficient, consistent, configurable enterprise workflow interface

## 2. Brand Direction

- Core brand framing: enterprise-grade design and development solution
- Tonal keywords: precise, efficient, calm, rational, modern, systemized, trustworthy
- Source-backed value cues from the official design guidance:
  - consistent rules keep the whole system coordinated
  - rhythmic visual cadence builds recognizable product beauty
  - clear direction improves efficiency
  - openness and inclusiveness help solve problems
- Must feel like: a polished professional control plane that reduces cognitive friction
- Must not feel like: playful consumer app UI, overly decorative landing page, glassmorphism-heavy concept shot, or soft pastel lifestyle product

## 3. Visual Style

- Overall direction: restrained enterprise UI with clean white surfaces, clear segmentation, and blue-led emphasis
- Density: balanced-to-compact rather than spacious
- Surface strategy: mostly white backgrounds and white cards on light neutral canvas
- Shape language:
  - default component corner radius: 4px
  - larger containers and highlighted blocks may use 8px
  - circular and full-round shapes are allowed for icon actions and round buttons
- Depth strategy: minimal shadows, rely more on borders, spacing, and card separation than dramatic elevation
- Background treatment: keep app backgrounds plain and neutral, avoid noisy textures or large decorative gradients in the product shell
- Iconography: simple line-based product icons that align with the component system's visual weight

## 4. Color System

- Primary palette:
  - `primary-1`: `rgb(232,243,255)`
  - `primary-2`: `rgb(190,218,255)`
  - `primary-3`: `rgb(148,191,255)`
  - `primary-4`: `rgb(106,161,255)`
  - `primary-5`: `rgb(64,128,255)`
  - `primary-6`: `rgb(22,93,255)` and use this as the main action color
  - `primary-7`: `rgb(14,66,210)`
  - `primary-8`: `rgb(7,44,166)`
  - `primary-9`: `rgb(3,26,121)`
- Neutral light theme tokens:
  - `bg-1` to `bg-5`: `#fff`
  - `text-1`: `var(--color-neutral-10)`
  - `text-2`: `var(--color-neutral-8)`
  - `text-3`: `var(--color-neutral-6)`
  - `text-4`: `var(--color-neutral-4)`
  - `border-1`: `var(--color-neutral-2)`
  - `border-2`: `var(--color-neutral-3)`
  - `border-3`: `var(--color-neutral-4)`
  - `border-4`: `var(--color-neutral-6)`
- Dark theme support exists in the reference system, but the default generation target should be light theme unless the user explicitly requests dark mode.
- Semantic palettes:
  - success uses green tokens
  - warning uses yellow/orange tokens
  - danger uses red tokens
- Color usage rules:
  - use blue primarily for key actions, selected states, links, progress cues, and chart emphasis
  - keep non-active chrome neutral
  - do not overload pages with many saturated accent colors
  - reserve red, orange, and green for status semantics first, decoration second

## 5. Typography

- Font direction: modern sans-serif stack suitable for mixed Chinese and English enterprise products
- Hierarchy style: clear but restrained; typography should organize information, not dominate the UI
- Practical scale for generation:
  - page title: 20 to 24px, medium weight
  - section title: 16px
  - card title: 14 to 16px
  - body text: 14px
  - helper or metadata text: 12px
- Body tone: readable, low-drama, compact, optimized for repeated scanning
- Text color rules:
  - primary content uses `text-1`
  - secondary labels and descriptions use `text-2`
  - placeholders and supporting metadata use `text-3` or `text-4`
- Text casing: sentence case preferred; avoid all-caps dashboard labels

## 6. Layout and Spacing

- Shell pattern:
  - fixed top navbar enabled by default
  - left navigation menu enabled by default
  - footer optional but supported
- Key layout constants observed from the reference SaaS system:
  - top navbar height: `60px`
  - default menu width: `220px`
  - content wrapper top/side padding: `16px 20px 0`
  - breadcrumb bottom margin: `16px`
  - common block spacing: `24px`
- Content strategy:
  - maintain a clear shell-content separation
  - use cards and sections to divide dense information into manageable chunks
  - prefer aligned grids over asymmetrical artistic layouts
- Container behavior:
  - desktop-first with minimum width expectations around `1100px`
  - internal sections should still collapse sensibly on narrower screens
- Card padding:
  - default card body padding: `20px`
  - small card body padding: `16px`

## 7. Components

### Buttons

- Button families observed in the Figma library:
  - primary
  - secondary
  - dashed
  - outline
  - text or link-like lightweight actions
  - icon-only variants
- States:
  - default
  - hover
  - focus
  - active
  - disabled
- Sizes confirmed across Figma and CSS:
  - mini: `24px`
  - small: `28px`
  - default/medium: `32px`
  - large: `36px`
- Shapes:
  - rectangle with 4px radius
  - round pill variants
  - square icon buttons
  - circular icon buttons
- Usage rules:
  - one primary action per local action group whenever possible
  - secondary and outline actions should support, not compete with, the primary action
  - icon-only actions belong to toolbars and dense operational zones

### Inputs

- Inputs should follow the same radius and compact enterprise sizing as buttons
- Search inputs and settings search are often rounder than standard fields
- Form controls should favor clarity over decorative styling
- Validation should rely on semantic colors and concise helper text

### Cards

- Cards are the main surface primitive for dashboards and settings pages
- Default card body padding: `20px`
- Small card body padding: `16px`
- Cards should be visually quiet and let data density do the work
- Use cards to group stats, charts, announcements, quick actions, and profile sections

### Navigation

- Navigation shell should be stable and unobtrusive
- Top navbar includes global search, language, theme toggles, notifications, and user menu
- Left nav holds the main information architecture
- Active states should be obvious via color and selected styling, not ornamental treatment

### Data Visualization

- Visualization pages should balance KPI cards, charts, trend modules, and commentary blocks
- Use blue as the primary highlight color, with semantic colors for warnings and anomalies
- Keep chart areas inside clean cards with clear headings and supporting labels

## 8. Motion

- Motion principle: subtle, utilitarian, and feedback-oriented
- Motion should reinforce state change, disclosure, loading, and navigation clarity
- Avoid dramatic transitions and decorative motion sequences in enterprise product flows
- Hover, collapse, and layout transitions should feel crisp and lightweight

## 9. Content Style

- Writing tone: concise, neutral, operational
- CTA tone: direct and task-oriented
- Empty states: brief, calm, informative
- Dashboard copy: emphasize what changed, what needs attention, and what can be acted on next
- Settings copy: explanatory but compact
- Avoid generic demo wording in visible product chrome
- Prefer one coherent business domain per page
- KPI labels, filter fields, statuses, and actions should describe a believable operational workflow

## 10. Accessibility

- Preserve clear semantic color roles and adequate text contrast
- Ensure focus states remain visible for keyboard users
- Keep icon-only actions large enough to remain discoverable and clickable
- Dense layouts are acceptable only when hierarchy and spacing still support fast scanning

## 11. Data-Dense Page Rules

- High-density pages should feel compressed but not cramped.
- Use whitespace rhythm to separate blocks even when the page contains a lot of controls.
- Prefer consistent alignment over trying to fit every possible module above the fold.
- If a page becomes too dense, reduce decorative chrome before reducing readability.
- Use summary cards only when they support the operator's first decision on the page.

## 12. Page-Level Rules

- Every page should have one dominant purpose visible near the top.
- Use breadcrumb plus title for deeper platform pages when navigation context matters.
- Mix high-level summary modules with detailed operational modules; do not flatten everything into a single long table.
- On dashboard pages, place summary cards and high-priority modules above secondary lists.
- On management pages, put filters above tables and bulk actions near the dataset.
- On settings and profile pages, group information into clear blocks such as header, info, security, and verification.
- On management pages, keep toolbar utilities distinct from filter actions and distinct from the page-level CTA.

## 13. List Page Layout Rules

- Treat list pages as systems, not screenshots.
- Determine the list family first:
  - search table
  - card list
  - hybrid list
  - hierarchical list
- Determine filter density from business needs, not from the reference screenshot's row count.
- Always separate:
  - page-level CTA
  - filter actions
  - table or list utility actions
  - bulk actions
- Filter row strategy:
  - 1 row when the workflow is light
  - 2 rows for common operational list pages
  - 3 rows when several dimensions are genuinely needed
  - more than 3 visible rows should trigger restructuring rather than blind wrapping
- When filters grow:
  - preserve minimum usable control widths
  - wrap by logical control groups
  - move low-priority filters into advanced or expandable sections
  - keep Tier A filters always visible
- Toolbar strategy:
  - left side for selection count and bulk actions
  - right side for refresh, density, export, column settings, and view switches
- If the same dataset has table and card views, keep the filter logic and sorting semantics stable across both views.

## 14. Review And QA Rules

- Before presenting generated work, check language consistency, content realism, and layout elasticity.
- Do not stop after component placement; verify labels, statuses, actions, and example data still fit the page goal.
- A page should pass both visual consistency checks and workflow plausibility checks.

## 15. Non-Negotiables

- Do not replace the blue-led action hierarchy with unrelated accent-led palettes.
- Do not use oversized hero marketing sections or decorative editorial layouts for product pages.
- Do not use soft-card consumer styling, glassmorphism, neon gradients, or playful illustration-heavy treatments in core SaaS screens.
- Do not remove compact operational affordances such as filters, quick actions, or dense card modules when the page goal requires them.
- Do not hardcode a fixed number of filter rows from any one reference page.
- Do not present component-library placeholder copy as final product content.
