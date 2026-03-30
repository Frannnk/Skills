# SaaS Example Page Breakdowns

Use this file when the task needs more than a route match. This is the deeper, page-by-page breakdown layer built from the supplied demo routes, bundle inspection, and design-pattern inference.

Treat these as structural references, not screenshot templates.

## 1. `dashboard/workplace`

### Primary job

- orient the user immediately after login
- combine overview, shortcuts, and recent or recommended content

### Typical block order

1. page context or welcome block
2. top summary area
3. mixed secondary modules
4. recent activity, docs, recommendations, or shortcut modules

### Reusable modules

- overview metrics
- announcement or notice panel
- docs or knowledge entry
- shortcuts
- popular contents
- carousel or rotating attention block

### Generation notes

- keep the top region broader and more welcoming than a management list page
- mix information and action blocks instead of stacking only tables
- use this page when the user says “工作台”, “首页”, “进入系统后的第一屏”

## 2. `dashboard/monitor`

### Primary job

- expose operational status and recent activity
- support repeated scanning through the day

### Typical block order

1. status summary
2. key metric cards
3. quick operation block
4. recent message or communication block
5. supporting lists or live activity panels

### Reusable modules

- studio or workspace status
- quick operation
- data statistic
- data statistic list
- message list
- chat panel

### Generation notes

- do not turn this into an alarm wall unless the task is explicitly high-severity monitoring
- the layout should privilege “what changed” and “what needs response”
- use this page when the user says “监控”, “实时状态”, “运营看板”, “告警与消息”

## 3. `visualization/data-analysis`

### Primary job

- help users judge business health from KPIs and trends

### Typical block order

1. KPI summary row
2. main trend modules
3. comparative or segmented charts
4. interpretation, commentary, or public-opinion style block

### Reusable modules

- KPI cards
- trend charts
- comparison charts
- analysis commentary

### Generation notes

- lead with the numbers that define the story
- charts should live in quiet cards with strong headings
- use this page for “分析页”, “数据看板”, “趋势分析”, “经营洞察”

## 4. `visualization/multi-dimension-data-analysis`

### Primary job

- compare metrics across dimensions, groups, or scenarios

### Typical block order

1. dimension selectors
2. KPI and top comparison block
3. chart groups by business question
4. deeper segmented comparisons

### Reusable modules

- multiple filter dimensions
- comparison charts
- segmented KPI summaries
- grouped chart cards

### Generation notes

- organize by question, not by chart type
- this page can tolerate more filter complexity than a standard analytics page
- use when the user mentions “多维”, “分群”, “分地区”, “多口径对比”

## 5. `list/search-table`

### Primary job

- find, narrow, inspect, and operate on structured records

### Typical block order

1. page context
2. optional KPI row
3. search and filter block
4. table toolbar
5. result table
6. pagination

### Reusable modules

- search input
- inline or multi-row filters
- bulk actions
- utility actions
- compact operational table

### Generation notes

- this is the default management page pattern
- use when the user says “管理”, “查询”, “筛选”, “批量操作”, “表格”
- combine with `LIST_LAYOUT_RULES.md` for row elasticity

## 6. `list/card`

### Primary job

- browse richer entities that need more than a single row

### Typical block order

1. page context
2. filter and sort controls
3. optional tabs or view switch
4. card grid or card list
5. pagination

### Reusable modules

- sort controls
- filter bar
- card grid
- per-card status and lightweight actions

### Generation notes

- use for assets, templates, campaigns, libraries, or richer content objects
- card structure should stay highly repeatable
- if the same data could also work in a table, keep the logic consistent

## 7. `list/index`

### Primary job

- act as a neutral baseline list layout

### Typical block order

1. page context
2. optional scope controls
3. general list container
4. repeated item rows or grouped list areas

### Reusable modules

- baseline list scaffold
- moderate utility chrome
- standard list rhythm

### Generation notes

- use when the page is clearly list-oriented but not yet strongly table-first or card-first
- this is a good fallback when requirements are broad or still forming

## 8. `list/item`

### Primary job

- present repeated list items with richer per-item structure than a dense table row

### Typical block order

1. page context
2. list controls
3. repeated item blocks

### Reusable modules

- item identity
- metadata cluster
- trailing actions
- grouped secondary information

### Generation notes

- use when each row needs more structure than a table can comfortably hold
- useful for task queues, review queues, or content review pages

## 9. `list/style`

### Primary job

- provide alternate list presentation patterns

### Typical block order

1. page context
2. list controls
3. stylized item list or grouped result views

### Reusable modules

- alternate row treatments
- grouped result sections
- softer list rhythm than pure operational tables

### Generation notes

- use when the user still needs a list but wants a lighter, less tabular presentation

## 10. `form/group`

### Primary job

- collect or edit a large amount of structured information

### Typical block order

1. page title and context
2. grouped form sections
3. inline help and validation
4. submit and secondary actions

### Reusable modules

- section headers
- grouped inputs
- contextual help
- footer action row

### Generation notes

- align labels and controls cleanly
- use when the user says “配置页”, “编辑页”, “长表单”

## 11. `form/step`

### Primary job

- guide the user through staged input or setup

### Typical block order

1. step indicator
2. current step content
3. navigation actions
4. summary or confirmation

### Reusable modules

- stepper
- focused step card
- next and previous actions
- summary state

### Generation notes

- each step should expose only what is needed right now
- use when the process benefits from reduced cognitive load

## 12. `profile/basic`

### Primary job

- summarize one entity and then expose its details

### Typical block order

1. summary header
2. identity or overview block
3. grouped detail sections
4. secondary actions

### Reusable modules

- identity header
- detail cards
- grouped metadata

### Generation notes

- use for accounts, organizations, projects, or other “one object overview” pages

## 13. `user/info`

### Primary job

- show detailed account or identity information

### Typical block order

1. identity summary
2. grouped info sections
3. editable or secondary panels

### Reusable modules

- account summary
- contact information
- permission or related-record blocks

### Generation notes

- stronger on detail than `profile/basic`
- use when the page is clearly about one user's information structure

## 14. `user/setting`

### Primary job

- organize account or system settings into clear sections

### Typical block order

1. page title and summary
2. header or profile block
3. info section
4. security section
5. verification or status section

### Reusable modules

- profile summary
- editable information card
- security card
- verification card

### Generation notes

- preserve section boundaries strongly
- use when the user mentions “设置”, “安全设置”, “账号偏好”

## 15. `user/login`

### Primary job

- authenticate the user efficiently

### Typical block order

1. centered form or split auth layout
2. primary login action
3. secondary recovery or alternate auth actions

### Reusable modules

- login form
- brand marker
- supporting recovery links

### Generation notes

- keep the page sparse and controlled
- do not import the density of a dashboard into this screen

## 16. `user/user`

### Primary job

- handle a user-centered page that blends identity, status, and actions

### Typical block order

1. user summary
2. key management or activity module
3. grouped detail or related modules

### Reusable modules

- identity header
- user status
- actionable submodules

### Generation notes

- use when the request is user-centric but broader than just profile or settings

## 17. `result/success`

### Primary job

- confirm successful completion of a workflow

### Typical block order

1. success icon or state graphic
2. result title and description
3. primary next action
4. secondary actions

### Generation notes

- keep the layout sparse
- emphasize confidence and clear next steps

## 18. `result/error`

### Primary job

- explain a failed completion and give recovery paths

### Typical block order

1. error state graphic
2. explanation
3. retry or return actions

### Generation notes

- error pages should stay calm and useful, not dramatic

## 19. `exception/403`

### Primary job

- explain access denial

### Typical block order

1. exception illustration or icon
2. title
3. cause or permission explanation
4. recovery action

## 20. `exception/404`

### Primary job

- explain missing resource

### Typical block order

1. exception illustration or icon
2. title
3. short explanation
4. navigation recovery action

## 21. `exception/500`

### Primary job

- explain system failure

### Typical block order

1. exception illustration or icon
2. title
3. short system explanation
4. retry or return action

## 22. Cross-Page Extraction Rules

- Prefer extracting:
  - block order
  - information hierarchy
  - action hierarchy
  - density strategy
  - repeated module types
- Avoid copying:
  - literal card counts
  - exact filler text
  - arbitrary screenshot spacing that conflicts with the actual content needs
