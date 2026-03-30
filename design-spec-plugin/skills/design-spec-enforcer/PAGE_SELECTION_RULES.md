# SaaS Page Selection Rules

Use this file to decide which page family to generate before touching layout details. The purpose is to avoid picking a page pattern by vibe alone.

## 1. Selection Order

Always decide in this order:

1. What is the page's primary job
2. What is the dominant result surface
3. What is the interaction density
4. Whether the user needs a known example route family
5. Whether the page is a hybrid and should borrow from two families

## 2. Primary Job Mapping

### Dashboard

Use when the page's main job is:

- orienting the user after login
- showing current status, alerts, priorities, or summaries
- mixing overview, shortcuts, and recent activity

Prefer:

- `dashboard/workplace` for daily landing pages
- `dashboard/monitor` for live operational pages

### Analytics

Use when the page's main job is:

- understanding trends
- comparing segments
- interpreting metrics
- supporting business decisions with charts

Prefer:

- `visualization/data-analysis` for standard KPI and trend analysis
- `visualization/multi-dimension-data-analysis` for segmented or dimension-heavy analysis

### List Management

Use when the page's main job is:

- finding records
- filtering structured entities
- taking row-level or batch actions

Prefer:

- `list/search-table` for operational tables
- `list/card` for richer entity cards
- `list/index`, `list/item`, or `list/style` when the request is still a list page but the exact surface is less specialized

### Form Workflow

Use when the page's main job is:

- entering or editing structured information
- completing a guided workflow

Prefer:

- `form/group` for multi-section forms
- `form/step` for staged submission flows

### Identity, Profile, and Settings

Use when the page's main job is:

- showing one person, account, team, or object
- exposing grouped editable settings

Prefer:

- `profile/basic` for overview-style pages
- `user/info` for detail-heavy identity pages
- `user/setting` for grouped settings
- `user/user` when the request is user-centric but spans more than profile-only or settings-only concerns

### Entry or Outcome

Use when the page's main job is:

- authenticating the user
- confirming success
- reporting a failure
- handling exceptional routing states

Prefer:

- `user/login` for entry
- `result/success` or `result/error` for workflow outcomes
- `exception/403`, `exception/404`, `exception/500` for route or system exceptions

## 3. Dominant Result Surface

If the page is ambiguous, let the result surface decide:

- table dominates -> search table family
- repeated cards dominate -> card list family
- charts dominate -> analytics family
- forms dominate -> form family
- one entity overview dominates -> profile or user family

## 4. Hybrid Rules

Use a hybrid page when:

- the top half behaves like a dashboard but the bottom half is clearly a management list
- the same dataset needs both card and table views
- one page contains a summary shell plus a dense result surface

Hybrid rules:

- choose one primary family and one secondary family
- keep one hierarchy, not two competing page tops
- if the result surface is still the main task, list rules win over dashboard rules

## 5. User-Request Triggers

These phrases strongly suggest a family:

- “工作台”, “首页”, “概览” -> workplace dashboard
- “监控”, “告警”, “实时状态” -> monitor dashboard
- “分析”, “趋势”, “看板”, “洞察” -> analytics
- “管理”, “列表”, “筛选”, “批量操作”, “表格” -> list management
- “卡片列表”, “资源库”, “模板库”, “内容库” -> card list
- “创建”, “编辑”, “配置”, “提交” -> form workflow
- “详情”, “资料”, “个人信息” -> profile or user info
- “设置”, “安全”, “偏好” -> settings
- “登录” -> entry
- “成功页”, “失败页”, “错误页”, “异常页” -> result or exception

## 6. Tie-Breaker Rules

If multiple families seem plausible:

- choose the family that best matches the page's main task after first load
- choose the family that governs the biggest content area
- choose the family that owns the most important user action
- only use hybrid if both families are genuinely first-class

## 7. Output Requirement

Before generating, silently decide and internally record:

- selected family
- nearest example route
- whether the page is pure or hybrid
- why this family was chosen over nearby alternatives
