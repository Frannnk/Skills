# SaaS Design Prompt Templates

Use these templates as the default prompt layer for page generation and review. Replace bracketed parts with your own context.

## 1. Universal Page Generation Template

```md
Use my SaaS Design Spec Plugin to design a [page type] for [product or feature].

Goal:
- [primary business goal]

Users:
- [target users]

Required modules:
- [module 1]
- [module 2]
- [module 3]

Primary actions:
- [primary action]

Secondary actions:
- [secondary action]

Important data or states:
- [metric, field, or state]

Requirements:
- Follow the local SaaS design spec and nearest matching page pattern.
- Keep the hierarchy clear and enterprise-oriented.
- Use compact but readable spacing and restrained surfaces.
- Include loading, empty, and error considerations where appropriate.
- Summarize the rules you applied.
```

## 2. Workplace Dashboard Template

```md
Design a workplace dashboard for [product/team].

Include:
- top summary area with key KPIs
- announcement or notice block
- quick actions or shortcuts
- recent activity or popular content block
- one additional operational module tied to [business focus]

Requirements:
- Follow the workplace dashboard page pattern.
- Make it feel like a daily starting point for operators.
- Balance summary cards with actionable widgets.
- Keep the visual tone calm, efficient, and platform-like.
```

## 3. Monitor Dashboard Template

```md
Design a monitoring dashboard for [system/process].

Include:
- live status summary
- metric cards
- recent alerts or message list
- quick operation area
- one communication or coordination block

Requirements:
- Follow the monitor dashboard page pattern.
- Emphasize current status and urgency without turning the page into a warning wall.
- Keep the layout highly scannable for repeated use.
```

## 4. Analytics Page Template

```md
Design a data analysis page for [business domain].

Include:
- KPI summary cards
- trend chart area
- comparison section
- detailed breakdown section
- commentary or interpretation area

Requirements:
- Follow the analytics page pattern.
- Use charts inside clean cards with strong titles and supporting labels.
- Keep color usage disciplined and semantic.
- Prioritize decision-making clarity over visual novelty.
```

## 5. Search Table Page Template

```md
Design a search table page for [entity type].

Include:
- filter/search form
- table toolbar
- main data table
- row actions
- bulk actions

Requirements:
- Follow the search table page pattern.
- Put filters above the table.
- Keep the page dense but easy to scan.
- Make states and actions immediately understandable.
```

## 6. Card List Page Template

```md
Design a card list page for [entity type].

Include:
- top filter and sort controls
- repeating summary cards
- status indicators
- lightweight per-card actions

Requirements:
- Follow the card list page pattern.
- Keep cards structurally consistent.
- Avoid decorative variation that reduces scanning speed.
```

## 7. Group Form Template

```md
Design a grouped form page for [workflow].

Include:
- page title and context
- grouped sections with clear subheadings
- primary submit action
- secondary cancel or save-draft action
- validation and helper text behavior

Requirements:
- Follow the grouped form page pattern.
- Keep alignment clean and section rhythm consistent.
- Reduce fatigue for long-form completion.
```

## 8. Step Form Template

```md
Design a step form for [workflow].

Include:
- step indicator
- focused current-step content
- previous and next actions
- final confirmation summary

Requirements:
- Follow the step form page pattern.
- Show progression clearly.
- Do not overload a single step with unrelated content.
```

## 9. Profile or Settings Template

```md
Design a [profile/settings] page for [user or entity].

Include:
- top summary header
- grouped info sections
- security or permissions section if relevant
- verification or status section if relevant
- edit actions in predictable locations

Requirements:
- Follow the nearest profile or settings page pattern.
- Keep sections modular and easy to navigate.
- Make the page useful both for viewing and editing.
```

## 10. Success, Error, and Exception Template

```md
Design a [success/error/exception] result page for [scenario].

Include:
- clear status illustration or icon treatment
- concise explanation
- one primary next action
- one or two secondary actions

Requirements:
- Follow the result or exception page pattern.
- Keep the layout sparse and calm.
- Ensure recovery paths are obvious.
```

## 11. Design Review Template

```md
Review this page against my SaaS design spec.

Check:
- page hierarchy
- shell and navigation structure
- spacing rhythm
- card and surface treatment
- button, input, and state consistency
- semantic color use
- fit with the nearest page pattern

Return:
- what matches the spec
- what violates the spec
- the highest-priority fixes first
```

## 12. Component Generation Template

```md
Design a [component name] for a SaaS platform.

Context:
- used on [page or flow]
- primary purpose: [purpose]
- states needed: [states]
- content density: [compact/balanced]

Requirements:
- Follow the local SaaS design spec.
- Reuse the documented radius, hierarchy, and semantic state logic.
- Make the component feel system-native rather than standalone.
```
