# SaaS State And Interaction Rules

Use this file to keep page states and interaction feedback consistent across generated designs.

Write these as flexible rules, not frozen mockup instructions.

## 1. State Priority

When a page or module can show multiple states, resolve them in this order:

1. blocking error
2. empty with explanation
3. loading or skeleton
4. normal content
5. selected, hover, focus, and active micro-states inside the normal content

## 2. Page-Level States

### Loading

- `Default`: show structure before details when the page layout is already known
- `Recommended`: use skeleton blocks that preserve final layout rhythm
- `Avoid`: replacing the whole page with a spinner if the shell and page structure can stay stable
- `Non-negotiable`: loading state should not destroy the user's sense of place in the page

### Empty

- `Default`: explain what is empty and what the user can do next
- `Recommended`: keep one primary recovery action
- `Avoid`: showing an empty table with no explanation if the page is truly empty
- `Non-negotiable`: empty states must still preserve the page's information hierarchy

### Error

- `Default`: explain what failed and what recovery path is available
- `Recommended`: use calm tone and one clear retry or fallback action
- `Avoid`: making the page look catastrophic unless the workflow truly is catastrophic
- `Non-negotiable`: users must understand whether they can retry, wait, or navigate elsewhere

## 3. List Page States

### Filtered Empty State

- `Default`: distinguish between “no data exists” and “no results match current filters”
- `Recommended`: offer reset filters or broaden scope when the empty state is filter-caused

### Table Loading State

- `Default`: keep table header and page chrome visible
- `Recommended`: use row skeletons or placeholder rows inside the result area
- `Avoid`: moving surrounding controls during loading

### Bulk Selection State

- `Default`: reveal bulk actions only when selection exists
- `Recommended`: show selection count clearly and close to the bulk action group
- `Non-negotiable`: bulk state should be clearly distinguishable from the normal toolbar state

## 4. Card And Dashboard States

### KPI Loading

- `Default`: keep card shells visible and swap numbers with placeholders
- `Avoid`: removing the whole KPI row when only values are loading

### Widget Empty State

- `Default`: empty widgets should stay in-grid and explain what is missing
- `Recommended`: let empty widgets still communicate their purpose

## 5. Form And Settings States

### Disabled

- `Default`: disabled controls should remain legible but visibly unavailable
- `Avoid`: making disabled controls so faint that users cannot read them

### Validation Error

- `Default`: localize the error near the field or group
- `Recommended`: pair semantic color with concise helper text
- `Non-negotiable`: the user must understand what to fix

### Success Or Saved Feedback

- `Default`: use lightweight inline or toast-level feedback for routine saves
- `Avoid`: turning small settings saves into full-page success pages

## 6. Interaction Feedback

### Hover

- `Default`: hover should be subtle and quick
- `Recommended`: use gentle background, border, or text emphasis rather than dramatic motion
- `Non-negotiable`: hover must not change layout unexpectedly

### Focus

- `Default`: focus state should be clearly visible for keyboard users
- `Non-negotiable`: never remove visible focus indication without a replacement

### Selected

- `Default`: selected state should be stronger than hover and weaker than destructive error emphasis
- `Recommended`: use semantic highlight tied to the primary action color

### Active Or Pressed

- `Default`: active states should feel slightly firmer than hover
- `Avoid`: over-animating pressed states in enterprise UI

## 7. State Consistency By Component Group

### Buttons

- should cover:
  - default
  - hover
  - focus
  - active
  - disabled

### Inputs And Selects

- should cover:
  - default
  - hover
  - focus
  - filled
  - error
  - disabled

### Tables

- should cover:
  - normal
  - hover row
  - selected row
  - loading
  - empty

### Tags

- should stay semantically stable across normal, dense, and selected contexts

## 8. Conflict Handling

- If the user explicitly asks for a different state treatment, follow the request unless it breaks clarity.
- Preserve the structure and meaning of states even when the visual treatment changes.
- Keep page-level stability stronger than micro-interaction flourish.
