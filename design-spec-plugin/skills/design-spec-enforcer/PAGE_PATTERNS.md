# SaaS Page Patterns

Use these page archetypes when generating or reviewing interfaces. Prefer one of these patterns before inventing a new layout.

The example demo inventory also includes these route references that should map back into the archetypes below:

- `list/index`
- `list/item`
- `list/style`
- `user/login`
- `user/user`

## 1. Workplace Dashboard

- Route reference: `dashboard/workplace`
- Typical purpose: first-stop overview for a logged-in operator
- Core modules observed from the reference SaaS template:
  - overview
  - announcement
  - docs
  - popular contents
  - shortcuts
  - carousel
- Composition rules:
  - top area should establish the user's current context and key metrics
  - include a mix of summary cards and lightweight operational widgets
  - use quick links and content recommendations to accelerate daily workflow

## 2. Monitor Dashboard

- Route reference: `dashboard/monitor`
- Typical purpose: live operational status and team activity
- Core modules observed from the reference SaaS template:
  - studio
  - studio status
  - studio information
  - quick operation
  - data statistic
  - data statistic list
  - message list
  - chat panel
- Composition rules:
  - highlight current system or team status early
  - combine structured metrics with recent message feeds
  - reserve the right side or lower sections for live communication and recent activity

## 3. Data Analysis Page

- Route reference: `visualization/data-analysis`
- Typical purpose: metrics storytelling and trend inspection
- Core modules observed from the reference SaaS template:
  - top-level analysis dashboard
  - public opinion block
  - public opinion cards
- Composition rules:
  - lead with KPI cards and trend summaries
  - follow with chart-heavy cards and comparison modules
  - include commentary or interpretation blocks where the data needs explanation

## 4. Multi-Dimension Data Analysis

- Route reference: `visualization/multi-dimension-data-analysis`
- Typical purpose: exploring segmented or multidimensional business metrics
- Composition rules:
  - use multiple filtering dimensions or comparison controls
  - group charts by question, not by chart type
  - keep labels and legends concise to avoid visual overload

## 5. Search Table Page

- Route reference: `list/search-table`
- Typical purpose: operational management of structured records
- Core modules observed from the reference SaaS template:
  - filter form
  - table
  - constants and view mode helpers
- Composition rules:
  - place search and filter controls above the table
  - keep filter rows elastic instead of fixed; support 1 to 3 visible rows without visual collapse
  - separate filter actions from toolbar utility actions
  - allow quick scanning with compact rows and restrained chrome
  - surface bulk actions, row actions, and status chips clearly but economically
  - classify the page by filter density and result complexity before deciding whether to show inline filters, wrapped rows, or expandable advanced filters

## 6. Card List Page

- Route reference: `list/card`
- Typical purpose: managing entities that benefit from card-based summaries
- Composition rules:
  - use repeatable cards for medium-detail objects
  - place filter, sort, and view controls near the top
  - keep the same filter logic and information hierarchy as a search-table page when the card list is just another representation of the same dataset
  - keep each card action set short and predictable

## 7. Hybrid Result List Page

- Route references:
  - `list/search-table`
  - `list/card`
- Typical purpose: one dataset that may be viewed as table, cards, or scoped lists
- Composition rules:
  - keep the page context, filters, and utility toolbar stable while the result surface changes
  - avoid rebuilding the top half of the page when switching result view
  - use the same primary filters and sorting semantics across views

## 8. Group Form Page

- Route reference: `form/group`
- Typical purpose: structured data entry with multiple related sections
- Composition rules:
  - split long forms into logical groups
  - use section titles and spacing to reduce fatigue
  - align labels and controls cleanly for fast completion

## 9. Step Form Page

- Route reference: `form/step`
- Typical purpose: multi-stage guided workflow
- Composition rules:
  - show progress clearly
  - only expose the inputs needed for the current step
  - keep summary and confirmation steps clean and confidence-building

## 10. Basic Profile Page

- Route reference: `profile/basic`
- Typical purpose: person, account, or entity overview
- Core observed structure:
  - index container
  - repeating item blocks
- Composition rules:
  - use a concise header summary
  - present detailed information in separate cards or sections
  - keep action buttons nearby but secondary to the identity overview

## 11. User Info Page

- Route reference: `user/info`
- Typical purpose: account or identity detail view
- Composition rules:
  - combine editable and read-only information without losing structure
  - group by identity, contact, permissions, and related records where relevant

## 12. User Settings Page

- Route reference: `user/setting`
- Core modules observed from the reference SaaS template:
  - header
  - info
  - security
  - verified
- Composition rules:
  - present settings in grouped sections rather than one long form
  - reserve prominent space for security and verification states
  - keep the page informative even before edits happen

## 13. Success and Error Result Pages

- Route references:
  - `result/success`
  - `result/error`
- Typical purpose: confirm outcome after completing a flow
- Composition rules:
  - keep the page sparse and centered on the outcome
  - show one primary next action and one or two secondary actions
  - use semantic iconography and status color without heavy decoration

## 14. Exception Pages

- Route references:
  - `exception/403`
  - `exception/404`
  - `exception/500`
- Typical purpose: route guard, missing resource, or system error handling
- Composition rules:
  - keep the cause understandable
  - offer a recovery path
  - use generous whitespace compared with data-heavy pages

## Shared Composition Heuristics

- Begin with shell context: breadcrumb, page title, and top actions where relevant.
- Prefer a small number of strong sections over many weak boxes.
- Use 24px section rhythm and 16px internal layout rhythm as the default starting point.
- Use cards as the default section container.
- Keep top-level actions right-aligned and content titles left-aligned unless the page pattern strongly suggests otherwise.
