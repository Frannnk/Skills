# Skills Repository / Skills 仓库

This repository contains reusable Codex skills and plugins for product design generation workflows.

这个仓库用于存放可复用的 Codex skills 和 plugins，重点服务于产品设计生成与设计规范工作流。

## Included / 仓库内容

### `design-spec-plugin`

A local Codex plugin for generating stable SaaS and admin-console interfaces from a structured design specification.

一个本地 Codex 插件，用结构化设计规范来生成更稳定的 SaaS 与后台管理界面。

What it includes:

包含的能力：

- page-family selection rules
- list-page layout rules
- component composition rules
- state and interaction rules
- language QA rules
- component-library mapping guidance
- prompt templates and brief templates
- backtest notes and release notes

- 页面类型选择规则
- 列表页布局规则
- 组件组合规则
- 状态与交互规则
- 文案与语言 QA 规则
- 组件库映射指引
- prompt 模板与 brief 模板
- 回测记录与发布说明

## Repository Structure / 仓库结构

```text
.
├── COMPATIBILITY.md
├── INSTALL.md
├── LICENSE
├── README.md
└── design-spec-plugin/
    ├── .codex-plugin/
    ├── skills/
    ├── assets/
    ├── examples/
    └── README.md
```

## Quick Use / 快速开始

If you are using Codex locally, point it at `design-spec-plugin` as a local plugin.

如果你在本地使用 Codex，可以把 `design-spec-plugin` 作为本地插件接入。

Useful entry files:

建议优先查看这些入口文件：

- `COMPATIBILITY.md`
- `INSTALL.md`
- `design-spec-plugin/README.md`
- `design-spec-plugin/QUICK_START.md`
- `design-spec-plugin/PLUGIN_CAPABILITIES.md`
- `design-spec-plugin/skills/design-spec-enforcer/SKILL.md`

## Tool Compatibility / 工具兼容性

- **Codex**
  - native target format
  - can be used directly as a local plugin
- **Claude**
  - not a native plugin format
  - use it as a rule pack or project knowledge source
- **Cursor**
  - not a native plugin format
  - use it as local documentation, prompt templates, and design rules

- **Codex**
  - 这是原生目标格式
  - 可以直接作为本地插件使用
- **Claude**
  - 不是原生插件格式
  - 更适合作为规则包或项目知识库使用
- **Cursor**
  - 不是原生插件格式
  - 更适合作为本地文档、prompt 模板和设计规则仓库使用

See:

详细说明见：

- `COMPATIBILITY.md`

## Notes / 说明

- The plugin is packaged as a local Codex plugin.
- Metadata for homepage and repository currently uses placeholder URLs and can be replaced later with the final public links.
- The plugin content is written as a neutral SaaS design system package and does not expose source-system branding in the public-facing rules.

- 这个插件当前以本地 Codex 插件形式组织。
- `plugin.json` 里的主页和仓库地址目前仍是占位 URL，后续可以替换成真实公开链接。
- 插件内容已经整理成中性的 SaaS 设计规范包，不会在公开规则里暴露参考系统品牌。
