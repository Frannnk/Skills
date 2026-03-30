# Quick Start

Use this file to start using the SaaS Design Spec Plugin quickly.

## 1. What This Plugin Is Good At

This plugin is designed for:

- enterprise SaaS dashboards
- management list pages
- analytics pages
- grouped forms
- settings and profile pages
- result and exception pages

It is strongest when you want:

- stable page structure
- consistent visual hierarchy
- better use of the published component library
- fewer demo-like labels and placeholder leftovers

## 2. Fastest Way To Use It

Say one sentence like:

```md
按我的 SaaS design spec，设计一个用户管理后台首页，要有概览卡片、筛选、表格和批量操作。
```

Or use the brief template:

[中文需求模板](./skills/design-spec-enforcer/BRIEF_TEMPLATE_ZH.md)
[English Brief Template](./skills/design-spec-enforcer/BRIEF_TEMPLATE.md)

## 3. Best Prompt Shape

For the most stable results, include:

- 页面类型
- 页面目标
- 目标用户
- 核心模块
- 主要操作
- 语言模式
- 状态要求
- 特殊限制

Example:

```md
页面类型：搜索表格页
页面目标：管理客户支持工单
目标用户：客服主管、客服专员
语言模式：zh-CN
核心模块：筛选栏、KPI 概览、工单表格、详情抽屉、批量操作
关键数据/指标：待处理工单、超时工单、SLA 风险、解决率
主要操作：分配工单、修改优先级、关闭工单
次要操作：导出、保存筛选视图、查看详情
需要覆盖的状态：
  - 默认
  - 加载中
  - 空状态
  - 错误状态
响应式优先级：桌面优先，平板可用
特殊限制：信息密度高，但必须清晰易扫读
```

## 4. Good Requests

- “设计一个客户工单搜索表格页，重点是筛选效率和批量处理”
- “设计一个运营工作台首页，强调最近动态和快捷操作”
- “设计一个账号设置页，分成资料、安全和认证三组”
- “审查这个页面是不是符合我的 SaaS design spec”

## 5. What The Plugin Will Do

The plugin will usually:

1. determine the nearest page family
2. match the nearest example route
3. select a suitable block structure
4. choose realistic KPIs, filters, columns, and actions
5. prefer component-library instances when available
6. self-check language, realism, state coverage, and layout clarity

## 6. When To Be More Explicit

Be more explicit when:

- you do not want KPI cards
- you want filters in a drawer instead of above the table
- you want card view instead of table view
- you want bilingual output
- you want an intentionally unusual page structure

Example:

```md
不要 KPI 卡片。
筛选区放右侧抽屉。
结果只要卡片视图，不要表格。
```

## 7. Useful Files

[Plugin Capabilities](./PLUGIN_CAPABILITIES.md)
[README](./README.md)
[Prompt Templates ZH](./skills/design-spec-enforcer/PROMPT_TEMPLATES_ZH.md)
[Design Spec](./skills/design-spec-enforcer/DESIGN_SPEC.md)
