# Research Sources

This plugin was shaped from the following source categories provided by the user plus direct token and bundle inspection.

## 1. Provided Component Library

- Observed directly through Figma MCP:
  - the supplied node points to the button library
  - the button system includes primary, secondary, dashed, outline, and icon-only variants
  - states include default, hover, focus, active, and disabled
  - sizes include mini, small, medium/default, and large
  - shapes include rectangle, full-round, square, and circle
- Strong inference from screenshot and metadata:
  - the source library favors systematic variant coverage rather than a small ad hoc button set
  - state and size discipline are central to the design system

## 2. Provided Design Guidance Site

- Extracted from page HTML and bundled site strings:
  - the guidance positions itself as an enterprise-grade design and development solution
  - the site exposes design resources for specification, principles, style guide, component usage, and admin-product best practices
  - the guidance emphasizes enterprise design systems, consistency, efficiency, and design-development collaboration
  - value statements visible in the bundle include:
    - consistent rules keep the system coordinated
    - rhythmic visual cadence forms product beauty
    - clear direction improves efficiency
    - openness and inclusiveness help solve problems

## 3. Provided Admin Demo

- Extracted from page HTML, CSS, and bundled route definitions:
  - theme color defaults to `#165DFF`
  - layout defaults include `navbar: true`, `menu: true`, `footer: true`, `menuWidth: 220`
  - layout navbar height is `60px`
  - content wrapper padding is `16px 20px 0`
  - breadcrumb margin bottom is `16px`
  - common block spacing is `24px`
  - default card body padding is `20px`, small card body padding is `16px`
  - main route groups include dashboard, visualization, list, form, profile, result, exception, and user
- Page archetypes confirmed from route bundle:
  - `dashboard/workplace`
  - `dashboard/monitor`
  - `visualization/data-analysis`
  - `visualization/multi-dimension-data-analysis`
  - `list/search-table`
  - `list/card`
  - `form/group`
  - `form/step`
  - `profile/basic`
  - `result/success`
  - `result/error`
  - `user/info`
  - `user/setting`
  - `exception/403`
  - `exception/404`
  - `exception/500`
- Internal module names extracted from the bundle:
  - workplace: overview, announcement, docs, popular contents, shortcuts, carousel
  - monitor: studio, studio status, studio information, quick operation, data statistic, data statistic list, message list, chat panel
  - user setting: header, info, security, verified

## 4. Theme Token Inspection

- Extracted values:
  - primary palette centers on `primary-6 = rgb(22,93,255)`
  - primary colors derive from a vivid enterprise-blue palette
  - radii include `2px`, `4px`, `8px`, and circular shapes
  - button heights align with `24px`, `28px`, `32px`, and `36px`
  - light theme backgrounds are white and text uses neutral scales
  - semantic feedback colors map to green, yellow/orange, and red token families

## Confidence Notes

- Token and layout constants above are direct extractions from shipped assets.
- Typography sizing beyond what is visible in CSS and screenshots includes some informed inference for practical generation.
- The Figma MCP session hit rate limits after the initial node inspection, so this plugin leans on the provided node metadata, screenshot, official docs HTML, and published Pro assets to complete the spec.
