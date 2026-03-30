# SaaS Content Realism Rules

Use this file to make generated pages feel like believable enterprise product screens instead of generic demos.

## 1. Core Principle

- Prefer realistic business language over abstract showcase wording.
- Prefer coherent datasets over random filler values.
- Prefer domain-shaped modules over a pile of generic cards, tables, and buttons.

## 2. Naming Rules

### Good labels

- user management
- customer tickets
- organization
- role permissions
- approval records
- campaign performance
- order fulfillment

### Avoid generic showcase copy

- demo data
- sample item
- test card
- module one
- content block
- table example
- chart example

## 3. KPI Rules

- KPI cards should represent metrics the operator would actually check first.
- Each KPI card should answer one of these questions:
  - what is the total volume
  - what changed recently
  - what needs attention
  - what is at risk
- Avoid four cards that all say nearly the same thing.

### Good KPI sets

- total users
- weekly new users
- active users
- risk accounts

- total orders
- pending shipment
- abnormal orders
- refund rate

## 4. Filter Rules

- Filters should come from how people actually narrow the dataset.
- Use a mix of:
  - identity fields
  - status fields
  - ownership fields
  - time fields
  - organizational fields
- Avoid adding fields only to make the form look rich.

## 5. Table Rules

- Every column should earn its space.
- Table columns should usually cover:
  - identity
  - core business attribute
  - state
  - owner or org
  - time
  - action
- Avoid random mixed columns that do not support one workflow.

## 6. Action Rules

- Primary actions should match the page goal.
- Bulk actions should be realistic for the entity type.
- Row actions should stay short and predictable.

### Good row actions

- view
- edit
- assign
- approve
- disable

### Avoid weak generic row actions

- click here
- do action
- process item

## 7. Status Rules

- Statuses should be finite, mutually understandable, and semantically colorable.
- Use operational states instead of vague adjectives.

### Better status sets

- active, pending, disabled, abnormal
- draft, scheduled, running, paused, completed
- pending review, approved, rejected, expired

## 8. Empty And Error States

- Empty states should say what is missing and what to do next.
- Error states should say what failed and what the user can try.
- Keep both concise and calm.

## 9. Domain Consistency

- Once a page is about one domain, all modules should reinforce that domain.
- Do not mix unrelated domains in one management page unless the page is intentionally cross-functional.

## 10. Realism QA

Check:

- whether the page could plausibly exist inside a real SaaS product
- whether the KPIs, filters, table fields, and actions describe one coherent workflow
- whether any text still sounds like a component-library demo
