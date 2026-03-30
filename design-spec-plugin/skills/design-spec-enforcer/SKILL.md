---
name: design-spec-enforcer
description: Read the local SaaS design specification and page patterns, then use them as hard constraints before generating, reviewing, or refining UI designs.
---

# Design Spec Enforcer

Use this skill whenever a task involves:

- creating a UI concept, screen, component, or layout
- refining an existing interface
- reviewing whether a design follows the user's rules
- translating a rough brief into a design direction

## Source of truth

Always read:

- `DESIGN_SPEC.md`
- `PAGE_PATTERNS.md`
- `LIST_LAYOUT_RULES.md`
- `EXAMPLE_PAGE_INDEX.md`
- `EXAMPLE_PAGE_BREAKDOWNS.md`
- `PAGE_SELECTION_RULES.md`
- `LANGUAGE_QA_RULES.md`
- `CONTENT_REALISM_RULES.md`
- `DESIGN_REVIEW_CHECKLIST.md`
- `HIGH_FREQUENCY_PAGE_RULES.md`
- `COMPONENT_COMPOSITION_RULES.md`
- `STATE_AND_INTERACTION_RULES.md`
- `COMPONENT_LIBRARY_MAPPING.md`
- `PROMPT_TEMPLATES.md`
- `BRIEF_TEMPLATE.md`
- `PROMPT_TEMPLATES_ZH.md`
- `BRIEF_TEMPLATE_ZH.md`
- `RESEARCH_SOURCES.md`

Treat `DESIGN_SPEC.md` as the main rule set, `PAGE_PATTERNS.md` as the composition guide for page-level output, `LIST_LAYOUT_RULES.md` as the dedicated rule set for list-heavy pages, `EXAMPLE_PAGE_INDEX.md` as the route-to-page-family map from the reference demo, `EXAMPLE_PAGE_BREAKDOWNS.md` as the route-to-block-structure layer, `PAGE_SELECTION_RULES.md` as the page-family decision layer, `LANGUAGE_QA_RULES.md` as the language and QA rule set, `CONTENT_REALISM_RULES.md` as the business-content realism layer, `DESIGN_REVIEW_CHECKLIST.md` as the final QA gate, `HIGH_FREQUENCY_PAGE_RULES.md` as the deeper rule layer for the most common page types, `COMPONENT_COMPOSITION_RULES.md` as the flexible component-group rule layer, `STATE_AND_INTERACTION_RULES.md` as the cross-page state and interaction layer, `COMPONENT_LIBRARY_MAPPING.md` as the bridge from design rules to the actual component library, and the prompt template files as the default prompting layer for generation and review tasks.

## Required workflow

1. Read `DESIGN_SPEC.md` and `PAGE_PATTERNS.md` before proposing or generating design work.
2. If the task is list-heavy, also read `LIST_LAYOUT_RULES.md` before deciding the filter area, toolbar, and result surface.
3. Read `EXAMPLE_PAGE_INDEX.md`, `EXAMPLE_PAGE_BREAKDOWNS.md`, and `PAGE_SELECTION_RULES.md` to map the request to the nearest example route or route family from the reference demo.
4. Determine the language mode and read `LANGUAGE_QA_RULES.md` before writing visible copy into the design.
5. Read `CONTENT_REALISM_RULES.md` before deciding KPI labels, filter fields, table columns, statuses, and actions.
6. If the task matches one of the most common page types, also read `HIGH_FREQUENCY_PAGE_RULES.md` and use the deeper page-specific guidance.
7. Read `COMPONENT_COMPOSITION_RULES.md` before deciding KPI groups, filter areas, toolbars, status tags, and settings sections.
8. Read `STATE_AND_INTERACTION_RULES.md` before deciding loading, empty, error, selected, hover, focus, and disabled treatments.
9. Read `COMPONENT_LIBRARY_MAPPING.md` before selecting library instances, variants, or override strategy in Figma-oriented generation.
10. Determine whether the task maps to one of the defined page archetypes:
   - workplace dashboard
   - monitor dashboard
   - analytics page
   - search table/list page
   - card list page
   - grouped form
   - step form
   - profile, settings, success, error, or exception page
11. Extract the constraints that matter for the current task:
   - brand attributes
   - target audience and product tone
   - layout and spacing rules
   - typography rules
   - color and contrast rules
   - component rules
   - motion rules
   - accessibility requirements
   - page composition rules
12. If the task is a new page generation task, start from the nearest prompt template.
13. Prefer `PROMPT_TEMPLATES_ZH.md` and `BRIEF_TEMPLATE_ZH.md` when the user is writing in Chinese.
14. If the user request is underspecified, use the nearest brief template as the missing-information checklist and make reasonable assumptions where low risk.
15. Apply those constraints explicitly in the design output.
16. Compose pages using the documented SaaS building blocks instead of inventing unrelated visual patterns.
17. For list pages, classify the page family first, then decide filter density, row count, and result surface. Never copy a fixed row count from a reference screenshot.
18. For all page types, prefer matching the nearest example family from `EXAMPLE_PAGE_INDEX.md`, then use `EXAMPLE_PAGE_BREAKDOWNS.md` to borrow the right block order and module pattern before inventing a new structure.
19. Treat `Non-negotiable` component and state rules as hard guardrails, but let `Default` and `Recommended` rules bend when the user prompt clearly asks for another structure.
20. When working in Figma or library-driven generation, use `COMPONENT_LIBRARY_MAPPING.md` to choose the closest library component before falling back to primitives.
21. In Figma or other library-driven generation, do not assume instance overrides succeeded just because the script succeeded. Run a screenshot-level check for visible placeholder leakage, especially on menu, select, statistic, and table components.
22. If a composite component keeps visible default copy after one correction pass, switch to a more reliable strategy from `COMPONENT_LIBRARY_MAPPING.md`: exposed property, safe-font text override, leaf component, then primitive wrapper.
23. After generating, self-check against `LANGUAGE_QA_RULES.md`, `CONTENT_REALISM_RULES.md`, `HIGH_FREQUENCY_PAGE_RULES.md`, `COMPONENT_COMPOSITION_RULES.md`, `STATE_AND_INTERACTION_RULES.md`, `COMPONENT_LIBRARY_MAPPING.md`, and `DESIGN_REVIEW_CHECKLIST.md` before presenting the result.
24. If the specification is incomplete, make conservative choices that stay aligned with the documented style.
25. If the user request conflicts with the spec, call out the conflict and prefer the spec unless the user clearly overrides it.

## Output rules

- Do not default to generic SaaS UI patterns when the documented page patterns define a clearer answer.
- Prefer the documented hierarchy: fixed top navbar, moderate left navigation, compact card grids, restrained surfaces, and clearly segmented content blocks.
- Reuse the documented button sizes, surface styles, radii, and semantic states.
- Keep the resulting design cohesive with the documented visual language.
- When reviewing a design, compare it against the spec section by section and point out concrete mismatches.
- When generating a new design, summarize the rules you applied in 3 to 6 short bullets before or after the design work, depending on what best fits the task.
- When the user asks for a page directly, prefer to silently map it to the closest built-in prompt template instead of asking them to structure the request manually.

## Files

- `DESIGN_SPEC.md`: design rules and conventions
- `PAGE_PATTERNS.md`: page composition patterns and archetypes
- `LIST_LAYOUT_RULES.md`: elastic rules for search forms, toolbars, tables, card lists, and hybrid list pages
- `EXAMPLE_PAGE_INDEX.md`: route inventory and page-family summaries extracted from the reference demo
- `EXAMPLE_PAGE_BREAKDOWNS.md`: page-by-page structural breakdowns for the example routes
- `PAGE_SELECTION_RULES.md`: decision rules for picking the right page family before generation
- `LANGUAGE_QA_RULES.md`: language consistency and post-generation QA checks
- `CONTENT_REALISM_RULES.md`: rules for realistic KPIs, filters, tables, statuses, and actions
- `DESIGN_REVIEW_CHECKLIST.md`: final review checklist for generation and QA
- `HIGH_FREQUENCY_PAGE_RULES.md`: deeper structural rules for the most common SaaS page types
- `COMPONENT_COMPOSITION_RULES.md`: flexible composition rules for KPI groups, filters, toolbars, status tags, and settings sections
- `STATE_AND_INTERACTION_RULES.md`: rules for loading, empty, error, hover, focus, selected, active, and disabled states
- `COMPONENT_LIBRARY_MAPPING.md`: high-frequency component families, search terms, override points, and fallback strategy for the library
- `PROMPT_TEMPLATES.md`: copy-ready generation and review prompts
- `BRIEF_TEMPLATE.md`: compact brief template for new page requests
- `PROMPT_TEMPLATES_ZH.md`: Chinese prompt templates for direct use
- `BRIEF_TEMPLATE_ZH.md`: Chinese brief template for direct use
- `RESEARCH_SOURCES.md`: source traceability and research notes

## Maintenance

When the user refines their visual system, update `DESIGN_SPEC.md` first and then adjust `PAGE_PATTERNS.md` if the composition rules also change.
