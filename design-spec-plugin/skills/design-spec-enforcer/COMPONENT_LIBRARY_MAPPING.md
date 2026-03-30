# SaaS Component Library Mapping

Use this file when generating with the published component library in Figma. It bridges page rules to actual component families, likely search terms, and known override behavior.

This file should guide component selection, not force one exact assembly every time.

## 1. Usage Principle

- Prefer library instances over custom-drawn primitives when the component is available and fits the task.
- Use primitives only when:
  - the needed component does not exist
  - the component does not support the required structure
  - the page needs a light wrapper around library instances
- When the user asks for a different structure, keep the library vocabulary but adapt the composition.

## 2. High-Priority Library Components

### Button

- Search terms:
  - `button`
- Known family:
  - `button`
- Known component key:
  - `fed8b92e983737cbb28fee35532482e2e93eaf38`
- Preferred usage:
  - page CTA
  - filter actions
  - toolbar actions
  - inline secondary actions
- Preferred variants:
  - primary for main CTA
  - secondary or outline for support actions
  - text or link-like for lighter operations
- Known override behavior:
  - label text is usually set through an internal text node named like `Button Text`
  - in Figma generation, rebinding the visible text node to a safe loaded font may be more reliable than trying to load the component's original font
- Placeholder risks:
  - `Primary Action`

### Card

- Search terms:
  - `card`
- Known family:
  - `card`
- Known component key:
  - `1a55ac383eff05150dc819a2a7cc65adb1ef1018`
- Preferred usage:
  - section container
  - dashboard module
  - settings group
- Preferred variants:
  - bordered, quiet cards for product surfaces
- Known override behavior:
  - title and body content often live in internal text nodes
- Placeholder risks:
  - `Sample Card`
  - `This is a subtitle`
  - `More`

### Input

- Search terms:
  - `input`
- Known family:
  - `input`
- Known component key:
  - `933b7db9c3219860db31c11e8dfdb2132500ab6d`
- Preferred usage:
  - dense form entry
  - standard filters
- Preferred variants:
  - compact operational styles
- Known override behavior:
  - a reliable text property is exposed as `替换文本#148903:1041`
- Placeholder risks:
  - generic placeholder text
  - `Sample Product`

### Search Box

- Search terms:
  - `search-box`
  - `search`
- Known family:
  - `search-box`
- Known component key:
  - `bb1275d6c03cbaff65e5b20a5add5deb48fa21b0`
- Preferred usage:
  - top search
  - first filter field in management pages
- Known override behavior:
  - exposes a text property for replacement text
  - also contains editable internal text nodes
- Placeholder risks:
  - `Search`

### Select

- Search terms:
  - `select`
- Known family:
  - `select`
- Known component key:
  - `de98d54cfa895aa8a4e3527776f22099aee5db78`
- Preferred usage:
  - enum filters
  - scoped choices
- Preferred variants:
  - default compact dropdown filter style
- Known override behavior:
  - displayed label often lives in an internal text node
  - direct visible-label replacement may be less reliable than input placeholder replacement
- Placeholder risks:
  - `All statuses`
  - `All roles`
  - `Select an option`
  - default category names from the library

### Table

- Search terms:
  - `table`
- Known families:
  - `table`
  - `header cell`
  - `text cell`
  - `action cell`
- Known component keys:
  - table: `8104fdd4c88e110285482705743528e505dbc3f5`
  - header cell: `00bd9f70ae6f15922fb0bf60a06b6b4d08e6a77c`
  - text cell: `ed5d1d877b8f8eeff200720a4776360401b34259`
  - action cell: `a2405ac6bbdbeca59ec122cad235520b08193412`
- Preferred usage:
  - structured management pages
  - compact operational grids
- Known override behavior:
  - header label usually via internal text node
  - content cells often require text-node replacement
  - action cells typically use short link-like labels such as view or edit
  - full localization is often more reliable with row or cell-level assembly than with one monolithic table instance
- Placeholder risks:
  - `Sample Product`
  - `View`
  - repeated `Generic Column`

### Tag

- Search terms:
  - `tag`
- Known family:
  - `tag`
- Known component key:
  - `69bc4665e9db1c9480c339d55dd1fc2074ad9027`
- Preferred usage:
  - status display
  - semantic labels
- Known override behavior:
  - often exposes text replacement through a component text property
- Placeholder risks:
  - generic demo statuses

### Avatar

- Search terms:
  - `avatar`
- Known families:
  - `Avatar`
  - `Avatar.Group`
  - `avatar+text` table cells
- Known component keys:
  - avatar: `3514097eff6e172f217f30b6a9582403c565dea3`
  - avatar group: `0cd16d7581b152407b9b116680877b8d734e0372`
  - avatar plus text table cell: `a7c5abd710687dc921903f78066fb2e1ef3b79f1`
- Preferred usage:
  - user context
  - assignee cells
  - profile summary

### Menu

- Search terms:
  - `menu`
  - `vertical-menu-item`
- Known families:
  - `menu`
  - `vertical-menu-item/1st-level`
  - `vertical-menu-item/2rd-level`
- Known component keys:
  - menu: `bf0113302f9c66db926d1d7216c6b171e762693a`
  - first-level vertical item set: `0fb1f71373104f3d5157a5a3c5ce9d880d3ee719`
- Preferred usage:
  - left nav shell
  - application IA
- Known override behavior:
  - item labels usually live in internal text nodes or nested item properties
  - overrides on the aggregated `menu` instance may not reliably propagate to every visible item label
  - first-level menu-item components are safer when deterministic navigation copy matters
- Placeholder risks:
  - `Menu Item 1`
  - `Menu Item 2`

### Statistic

- Search terms:
  - `statistic`
- Known family:
  - `statistic`
- Known component key:
  - `df46a9db37651e8e35c717c38f459e8b211c25dc`
- Preferred usage:
  - KPI summary blocks
  - compact dashboard highlights
- Known override behavior:
  - title usually in a statistic-title text layer
  - value in internal text nodes
  - optional nested action may need hiding
  - safe-font rebinding may be needed before changing title or value text in automation
- Placeholder risks:
  - `Metric Label`
  - `192,393`
  - `Primary Action`

### Table Avatar Text Cell

- Search terms:
  - `avatar+text`
- Known family:
  - `components/table-cell/avatar+text`
- Known component key:
  - `a7c5abd710687dc921903f78066fb2e1ef3b79f1`
- Preferred usage:
  - user name column
  - assignee column
  - richer identity cells

## 3. Page-Type Mapping

### Search Table Page

- Prefer:
  - search box
  - select
  - button
  - table header and text cells
  - action cell
  - tag
  - pagination if available
- Optional:
  - statistic for top KPIs

### Workplace Dashboard

- Prefer:
  - card
  - statistic
  - button
  - avatar
- Optional:
  - menu and global search components for shell areas

### Settings Page

- Prefer:
  - card
  - input
  - select
  - button
  - avatar
  - tag when status or verification state is needed

## 4. Reliability Rules For Library-Driven Generation

- Prefer exposed component properties over internal-text mutation whenever both are available.
- Prefer leaf-level components over monolithic composite components when:
  - text replacement must be deterministic
  - localization is strict
  - the page is dense and operational
- Use aggregate components mainly for speed, shell structure, or low-risk placeholders.
- If a composite component still leaks default copy after one correction pass, switch strategy instead of forcing more brittle overrides.

## 5. Fallback Strategy

When a library component does not cooperate, use this order:

1. exposed component properties
2. safe-font override on visible text nodes
3. smaller leaf component from the same family
4. primitive wrapper around reliable library atoms

## 6. Mandatory Validation

After any library-driven generation pass:

- inspect the screenshot, not just the node tree
- look specifically for `Menu Item`, `Sample Product`, `Generic Column`, `View`, `Select an option`, and default numeric demos
- treat unresolved visible placeholder leakage as a blocking issue for review

### Data Analysis Page

- Prefer:
  - card
  - statistic
  - tabs or segmented controls if available
- Use custom chart frames when charts are not represented by reusable components

## 4. Override Strategy

- Replace all visible demo copy before finalizing.
- If a component exposes a text property, prefer that.
- If not, replace the visible internal text node.
- Keep component instances intact whenever possible.
- If a nested instance blocks required content changes, use the smallest necessary override rather than redrawing the whole module.

## 5. Fallback Strategy

- If the library has the semantic component but not the exact business variant, reuse the closest component and override content.
- If the library lacks the needed wrapper, build a light structural frame around library components.
- If the library component is too rigid for the requirement, preserve the visual language with primitives rather than forcing a broken instance.
