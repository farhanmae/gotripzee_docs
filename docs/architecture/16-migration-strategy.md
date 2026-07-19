# Migration Strategy

## Document Control

| Field | Value |
|---|---|
| Document | Migration Strategy |
| Version | 1.0 |
| Status | Draft |
| Repository | farhanmae/gotripzee_docs |
| Related Documents | [Current System Assessment](./02-current-system-assessment.md), [Business Process Analysis (AS-IS)](./03-business-process-analysis-as-is.md), [Domain Model](./06-domain-model.md), [Database Design](./09-database-design.md), [Deployment Architecture](./15-deployment-architecture.md), [Testing Strategy](./17-testing-strategy.md) |

## 1. Purpose

This document defines the migration strategy from the current Drupal Commerce platform to the target React, Frappe, ERPNext, and MariaDB platform. It focuses on preserving business value while moving to the new domain model safely and incrementally.

## 2. Migration Goals

- preserve critical commercial and operational records
- migrate reusable product and package knowledge
- normalize data around Travel Product and Product Offering
- separate Booking, Reservation, and Allocation in the target model
- preserve customer and payment history where legally and operationally required
- avoid ERPNext core modifications
- reduce business disruption during cutover

## 3. Migration Principles

1. Migrate business concepts, not Drupal implementation details.
2. ERPNext-owned masters should be created or matched in ERPNext.
3. Travel-specific data should move into custom Frappe DocTypes.
4. Package data must become composition references, not duplicated service records.
5. Inventory must be normalized into shared resources and calendars.
6. Migration must be testable, repeatable, and reconciled.
7. Cutover must protect bookings, payments, and customer communication.

## 4. Migration Scope

| Data Area | Target Owner |
|---|---|
| Customers | ERPNext |
| Suppliers | ERPNext |
| Contacts and Addresses | ERPNext |
| Travel Products | Travel App |
| Product Offerings | Travel App |
| Package Components | Travel App |
| Bookings | Travel App |
| Payments / Invoices | ERPNext references and finance migration approach |
| Reservations | Travel App, generated or migrated where source data supports |
| Allocations | Travel App, migrated where source data exists or initialized as pending |
| Content / SEO | React CMS approach or Frappe content model depending final decision |
| Media | File storage with mapped references |

## 5. Migration Phases

```mermaid
flowchart LR
    A[Discovery] --> B[Mapping]
    B --> C[Prototype Migration]
    C --> D[Data Cleansing]
    D --> E[Trial Migration]
    E --> F[UAT Reconciliation]
    F --> G[Cutover]
    G --> H[Post-Cutover Support]
```

## 6. Source Data Assessment

The Drupal source should be assessed for:

- product bundles
- commerce product variations
- package-related fields
- order and order item history
- customer accounts
- enquiry and webform submissions
- payment references
- inventory fields and custom availability logic
- media and SEO metadata
- content pages and blog content

## 7. Target Mapping Strategy

| Source Concept | Target Concept |
|---|---|
| Drupal product bundle | Travel Product type |
| Drupal product variation | Product Offering where it represents sellable variant |
| Package product fields | Package Component references |
| Drupal order | Booking |
| Drupal order item | Booking Item |
| Availability fields | Inventory Resource / Inventory Calendar |
| Completed booking quantity | Reservation and/or Allocation history where inferable |
| Webform enquiry | Enquiry linked to ERPNext Customer/Lead |
| Drupal user | ERPNext/Frappe User and Customer mapping |

## 8. Data Cleansing

Required cleansing activities:

- normalize product names and slugs
- identify duplicate customers
- classify product types consistently
- separate package wrapper data from component product data
- validate price and currency data
- map images and media references
- identify incomplete booking/payment records
- identify inventory records that cannot be inferred safely

## 9. Migration Reconciliation

Reconciliation metrics:

- product count by type
- offering count by product
- package component count
- customer count
- booking count by status
- payment reference count
- migrated media count
- unmapped or exception records
- inventory resource count
- financial totals where applicable

## 10. Cutover Strategy

Recommended cutover pattern:

1. freeze high-risk Drupal data changes
2. export final source data
3. run validated migration scripts
4. reconcile critical totals
5. validate product catalog and booking flows
6. switch public frontend traffic
7. monitor payment, booking, and enquiry paths
8. keep Drupal read-only for reference during stabilization

## 11. Parallel Run Considerations

A short parallel run may be useful for:

- validating catalogue accuracy
- validating enquiry flow
- comparing booking totals
- confirming payment reconciliation
- training staff

Avoid long-term dual-write unless absolutely required. Dual-write increases reconciliation risk.

## 12. Risk Register

| Risk | Mitigation |
|---|---|
| Product data maps too closely to Drupal implementation | Use domain model as target, not source structure. |
| Package components are duplicated | Force component reference mapping. |
| Inventory cannot be inferred | Mark as migration exception and initialize operational inventory through controlled setup. |
| Customer duplicates | Use matching rules and manual review. |
| Payment history incomplete | Preserve references and reconcile through finance. |
| Cutover booking conflict | Use freeze window and final reconciliation. |

## 13. Migration Acceptance Criteria

Migration is acceptable when:

- core products are present as Travel Products
- offerings are mapped correctly
- packages reference reusable component products
- active bookings are available in target system
- customer records are linked to ERPNext ownership
- inventory baseline is validated
- payment references are traceable
- staff can operate critical workflows
- reports identify all unmigrated exceptions

## 14. Summary

The migration strategy moves GoTripzee from Drupal implementation structures to the target domain model. It prioritizes data quality, repeatability, reconciliation, and operational continuity while preserving ERPNext ownership boundaries and travel-specific Frappe app responsibilities.

## 15. Traceability to Next Documents

This document feeds into:

- [Testing Strategy](./17-testing-strategy.md)
- [Operational Runbook](./18-operational-runbook.md)
- [Roadmap](./19-roadmap.md)
