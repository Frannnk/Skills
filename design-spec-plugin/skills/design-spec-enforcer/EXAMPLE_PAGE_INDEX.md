# SaaS Example Page Index

This file indexes the example pages observed from the provided SaaS reference demo and turns them into reusable design guidance. Treat these as page examples and route references, not fixed screens to imitate literally.

## 1. Dashboard Family

### `dashboard/workplace`

- Family: workplace dashboard
- Primary role: daily landing page after login
- Reusable ideas:
  - top summary and welcome context
  - quick actions
  - recent activity or content modules
  - lightweight mixed widgets

### `dashboard/monitor`

- Family: monitor dashboard
- Primary role: live operational tracking
- Reusable ideas:
  - current status overview
  - alert or message feed
  - quick operations
  - recent team or system activity

## 2. Visualization Family

### `visualization/data-analysis`

- Family: analytics page
- Primary role: KPI and trend analysis
- Reusable ideas:
  - summary metrics
  - trend charts
  - comparison modules
  - interpretation or commentary blocks

### `visualization/multi-dimension-data-analysis`

- Family: advanced analytics page
- Primary role: segmented and multidimensional analysis
- Reusable ideas:
  - dimension selectors
  - segmented charts
  - comparative views
  - multiple questions answered in one screen

## 3. List Family

### `list/search-table`

- Family: search table
- Primary role: structured operational management
- Reusable ideas:
  - multi-priority filters
  - utility toolbar
  - row actions and bulk actions
  - compact status-rich table

### `list/card`

- Family: card list
- Primary role: richer entity browsing
- Reusable ideas:
  - filter and sort controls
  - repeatable item cards
  - lightweight item actions
  - same dataset can potentially share logic with table view

### `list/index`

- Family: generic list hub or baseline list page
- Primary role: broad list layout reference
- Reusable ideas:
  - neutral list scaffolding
  - baseline spacing and toolbar rhythm
  - use as a fallback when the requested list type is not strongly specialized

### `list/item`

- Family: list item pattern page
- Primary role: reference for list-row or item-block composition
- Reusable ideas:
  - item-level metadata arrangement
  - actions attached to repeated list entries
  - useful when the result surface is neither a dense table nor a full card

### `list/style`

- Family: list style variant page
- Primary role: alternate list presentation patterns
- Reusable ideas:
  - visual variants of list rows or grouped items
  - use when the user requests a lighter list style without changing the data model

## 4. Form Family

### `form/group`

- Family: grouped form
- Primary role: long structured data entry
- Reusable ideas:
  - sectioned fields
  - grouped labels and controls
  - fatigue-reducing rhythm

### `form/step`

- Family: step form
- Primary role: staged workflow completion
- Reusable ideas:
  - progress visibility
  - single-step focus
  - summary and confirmation

## 5. Profile Family

### `profile/basic`

- Family: basic profile
- Primary role: entity overview and details
- Reusable ideas:
  - concise top summary
  - grouped detail blocks
  - secondary editing actions

## 6. User Family

### `user/info`

- Family: user detail page
- Primary role: personal or account information detail
- Reusable ideas:
  - overview plus editable details
  - identity and contact grouping
  - permissions or related information sections

### `user/setting`

- Family: settings page
- Primary role: grouped account or system configuration
- Reusable ideas:
  - info section
  - security section
  - verification or status section
  - stable edit affordances

### `user/login`

- Family: login or entry page
- Primary role: authentication entry
- Reusable ideas:
  - sparse centered layout
  - clear form hierarchy
  - strong primary CTA
  - restrained branding

### `user/user`

- Family: user-centered management or profile variant
- Primary role: user-specific operational page
- Reusable ideas:
  - blend of identity, status, and actions
  - use when the request is user-centric but not purely a settings or info page

## 7. Result Family

### `result/success`

- Family: success result page
- Primary role: completion confirmation
- Reusable ideas:
  - centered success state
  - clear next action
  - restrained supporting actions

### `result/error`

- Family: error result page
- Primary role: failed completion state
- Reusable ideas:
  - plain explanation
  - recovery path
  - clear retry or back action

## 8. Exception Family

### `exception/403`

- Family: exception page
- Primary role: permission denial
- Reusable ideas:
  - access explanation
  - fallback route
  - minimal but calm presentation

### `exception/404`

- Family: exception page
- Primary role: missing resource
- Reusable ideas:
  - not-found explanation
  - navigation recovery path
  - whitespace-led composition

### `exception/500`

- Family: exception page
- Primary role: server or system error
- Reusable ideas:
  - system failure explanation
  - retry or return path
  - quiet high-contrast status treatment

## 9. Usage Rules

- Before generating a page, first match the request to one of these example routes or families.
- If the request sits between multiple examples, prefer the family over the exact route.
- Reuse the route as a behavioral reference, not as a frozen visual template.
- For list pages, always combine this file with `LIST_LAYOUT_RULES.md`.
