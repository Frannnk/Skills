# High-Frequency Page Rules

Use this file for the four page types that appear most often in enterprise SaaS generation. These rules go one level deeper than general page breakdowns.

## 1. `list/search-table`

### Use when

- the user needs record management
- the primary task is search, filtering, review, and operation
- the result set is structured and action-heavy

### Preferred structure

1. breadcrumb and page title
2. optional KPI strip when it helps triage work
3. filter block
4. toolbar block
5. table
6. pagination

### KPI guidance

- use KPI cards only when they help prioritize work
- 3 to 4 cards is the usual upper bound
- good categories:
  - total volume
  - new today or this week
  - active or in-progress
  - abnormal or risky

### Filter block guidance

- first row should contain:
  - keyword search
  - primary status
  - one or two business-critical filters
- later rows should contain:
  - role or owner
  - organization or source
  - time range
  - lower-priority dimensions
- search and reset belong to the filter block
- export, density, refresh, and column settings belong to the toolbar

### Table guidance

- first column should establish record identity
- actions column should stay concise
- status column should use semantic tags
- time columns should be easy to compare vertically

### Common mistakes

- too many decorative KPI cards
- putting utility actions inside the filter form
- shrinking controls to fit one row
- table columns that describe different workflows at once

## 2. `dashboard/workplace`

### Use when

- the page is the user's first stop after login
- the goal is orientation plus quick action

### Preferred structure

1. welcome or context header
2. overview block
3. mixed operational modules
4. content and shortcut modules

### Overview block guidance

- include 3 to 5 high-signal items
- metrics should feel broad and top-level, not too operationally narrow

### Module mix guidance

Good module types:

- announcements
- shortcuts
- recent tasks
- popular content
- docs
- recommendations

### Common mistakes

- making it look like a management table page
- stacking too many same-weight cards
- forgetting quick actions
- treating every module as equally urgent

## 3. `user/setting`

### Use when

- the page is about grouped account, profile, security, or preference configuration

### Preferred structure

1. page summary
2. profile or identity block
3. info block
4. security block
5. verification or status block

### Section guidance

- profile block:
  - avatar
  - identity summary
  - stable edit affordance
- info block:
  - editable business or contact fields
- security block:
  - password
  - device or login security
  - permission-relevant settings
- verification block:
  - trust or identity state
  - certification or confirmation progress

### Common mistakes

- one long undifferentiated form
- no separation between profile and security concerns
- too many equal-weight edit buttons
- settings that read like data-entry forms instead of configuration groups

## 4. `visualization/data-analysis`

### Use when

- the page needs to help users interpret business performance
- trend reading matters more than row-level operation

### Preferred structure

1. KPI summary
2. main trend area
3. comparison area
4. breakdown area
5. interpretation or conclusion area

### KPI guidance

- start with decision-driving metrics
- avoid vanity metrics unless the user explicitly needs them

### Chart guidance

- the first chart should answer the biggest business question
- later charts should deepen, compare, or segment the story
- commentary blocks are useful when the page is meant to support discussion, not only reading

### Common mistakes

- too many unrelated charts
- no narrative order
- all cards looking equally important
- using chart variety without business reason

## 5. Cross-Page Detail Rules

- title and breadcrumb should establish context quickly
- top-right actions should be few and clear
- summaries should appear before details
- section transitions should feel intentional
- default state should already communicate the main workflow clearly
