# SaaS Component Composition Rules

Use this file for high-frequency component groups that appear across many SaaS pages.

This file is intentionally written with rule strength labels so generation stays flexible.

## Rule Strength

- `Non-negotiable`: only break if the user explicitly overrides the system behavior and accepts the tradeoff
- `Default`: use this unless the request points elsewhere
- `Recommended`: strong default preference, but easy to override when the prompt needs a different shape
- `Avoid`: avoid by default, but not absolutely forbidden

## 1. KPI Card Group

### Purpose

- summarize the most decision-relevant numbers at the top of a dashboard or management page

### Rules

- `Default`: use KPI cards only when the page benefits from immediate summary before deeper interaction
- `Recommended`: keep KPI cards to 3 to 5 items
- `Recommended`: each card should answer a distinct question such as total, change, active, risk, or completion
- `Recommended`: KPI cards should use short labels and one dominant value
- `Avoid`: adding KPI cards only because the reference page had them
- `Avoid`: making all KPI cards visually identical when one of them is clearly the risk or attention metric
- `Non-negotiable`: KPI cards must support the actual page workflow, not just fill space

### Override handling

- if the user explicitly asks for no KPI cards, remove them
- if the user asks for more KPI cards, allow it, but preserve scanning clarity and distinct meanings

## 2. Filter Area

### Purpose

- narrow the result set before or during operational work

### Rules

- `Default`: place filters above the result surface on management pages
- `Default`: separate filter actions from toolbar utility actions
- `Recommended`: first row should contain the highest-priority fields
- `Recommended`: use 1 to 3 visible rows depending on content density
- `Recommended`: group filters by narrowing logic, not alphabetically
- `Avoid`: shrinking all controls to force one-row layout
- `Avoid`: placing export, density, or column settings inside the filter action cluster
- `Non-negotiable`: filter layout must remain readable when the field count grows

### Override handling

- if the user explicitly asks for advanced filters in a drawer or collapse area, keep the hierarchy but allow that structure
- if the user asks for a side filter panel instead of a top filter form, follow the request and preserve clear grouping

## 3. Table Toolbar

### Purpose

- host utility actions and selection-driven actions around the result surface

### Rules

- `Default`: left side for selection state and bulk actions
- `Default`: right side for utility actions such as refresh, density, export, and column settings
- `Recommended`: keep global CTA separate from selection or utility controls
- `Recommended`: bulk actions should appear only when they make sense for the dataset
- `Avoid`: mixing row actions into the table toolbar
- `Avoid`: letting toolbar controls visually overpower the page's main business action
- `Non-negotiable`: users should be able to tell apart page-level action, filter action, bulk action, and utility action

### Override handling

- if the user explicitly wants a compact merged toolbar, allow it only if action hierarchy still stays legible

## 4. Status Tags

### Purpose

- make state legible during fast scanning

### Rules

- `Default`: use status tags for operational states in tables, cards, and summaries
- `Recommended`: keep labels short and mutually understandable
- `Recommended`: map semantic color to state meaning
- `Recommended`: keep the status taxonomy finite and stable inside one page
- `Avoid`: mixing multiple similar states that users cannot distinguish quickly
- `Avoid`: using tags as decorative accents unrelated to workflow state
- `Non-negotiable`: tag color and wording must reinforce meaning, not obscure it

### Override handling

- if the user asks for a text-only status style, allow it, but maintain semantic clarity by typography and color

## 5. Settings Section Card

### Purpose

- organize settings or profile information into manageable configuration groups

### Rules

- `Default`: split settings into clear thematic cards or sections such as profile, info, security, and verification
- `Recommended`: each section should have one clear topic and one obvious edit path
- `Recommended`: use short descriptive helper text only when the setting benefits from explanation
- `Avoid`: turning the whole settings page into one long undifferentiated form
- `Avoid`: scattering edit actions evenly across every row when one sectional edit affordance would be clearer
- `Non-negotiable`: the user should understand what kind of settings they are changing before interacting

### Override handling

- if the user explicitly wants inline editable rows everywhere, allow it, but preserve section boundaries

## 6. Conflict Resolution

- `Non-negotiable` rules protect clarity, realism, and structural sanity
- `Default` rules are the starting point
- `Recommended` rules should bend when the prompt has a good reason
- `Avoid` rules warn about common failure modes, not absolute bans

When a user prompt clearly conflicts with a `Default` or `Recommended` rule:

- keep the user's requested structure
- preserve as much hierarchy and clarity as possible
- do not force the component group back into the reference shape
