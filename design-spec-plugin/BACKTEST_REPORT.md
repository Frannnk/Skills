# Backtest Report

This report summarizes a lightweight backtest against three realistic page types.

## Scope

Pages used for backtest:

1. user management search-table page
2. workplace dashboard
3. account settings page

## 1. User Management Search-Table Page

### What worked

- page family selection was stable
- filter above toolbar above table remained consistent
- KPI, filters, table, and batch actions fit the domain

### What drifted

- top KPI cards can become too generic if the prompt is too short
- utility actions may compete with page CTA if not clearly separated
- placeholder language leakage remains a real risk in component-library generation

### Rule improvements made

- strengthened content realism layer
- strengthened component-library placeholder cleanup layer
- strengthened toolbar versus filter separation

## 2. Workplace Dashboard

### What worked

- shell and overall block hierarchy stayed stable
- summary plus mixed widgets pattern mapped well

### What drifted

- without stronger rules, pages can lean too much toward management layout instead of landing-page-for-operators layout
- content modules may become too same-weight
- composite library instances kept some default copy visible even after a first override attempt
- menu-level overrides were less reliable than expected when using one aggregated menu instance

### Rule improvements made

- added deeper workplace page rules in high-frequency page guidance
- clarified that workplace pages need welcome or context, overview, and mixed action-content modules
- strengthened library-copy cleanup rules for composite instances
- clarified fallback from aggregate navigation components to leaf menu items when labels do not update reliably

## 3. Account Settings Page

### What worked

- profile, info, security, and verification grouping was easy to preserve
- settings pages stayed calmer than dashboards and list pages

### What drifted

- edit affordances can scatter too evenly if not explicitly constrained
- pages can become one long form when prompts are underspecified
- explicit field content still drifted back to library defaults in some form controls
- overly optimistic `FILL` sizing assumptions caused a generation error in the first pass

### Rule improvements made

- strengthened settings section card rules
- added clearer settings-page breakdown and high-frequency guidance
- strengthened explicit-width-first guidance for first-pass generation
- strengthened component override reliability rules for dense form rows

## Cross-Page Findings

### Major gains

- page-family selection is much stronger than earlier versions
- list-page flexibility is significantly better
- language consistency and realism now have explicit review gates

### Remaining risks

- niche components are still less modeled than high-frequency ones
- chart-heavy pages still need more case-by-case judgment
- Figma library overrides may still need manual inspection on uncommon components
- composite components can hide placeholder leakage until screenshot review
- font availability can block direct internal-text mutation on some library instances

## Figma Replay Notes

The March 30, 2026 replay in Figma validated the spec against two generated pages:

1. `Validation - Workplace Dashboard`
2. `Validation - Account Settings`

Observed high-value findings:

- page shells, spacing rhythm, and block hierarchy were stable enough for beta use
- library-driven generation was strong for avatar, statistic, tag, input, select, button, and table shell usage
- placeholder leakage remained visible in composite components such as navigation, filters, and table content
- monolithic menu and monolithic table components are less deterministic for text replacement than leaf-level building blocks
- screenshot review is mandatory because metadata and instance creation success do not guarantee visible copy replacement

Operational guidance added from this replay:

- prefer component properties first, then safe-font text overrides, then leaf components, then primitive wrappers
- treat visible placeholder leakage as a blocking issue, not a polish issue
- use explicit widths on the first composition pass for dense operational pages, then optimize with fill and hug once structure is stable

## Release Recommendation

- Internal use: ready
- Team beta: ready
- Public polished release: one more round of real-page testing would still help
