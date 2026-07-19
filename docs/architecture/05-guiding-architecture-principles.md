# Guiding Architecture Principles

## Document Control

| Field | Value |
|---|---|
| Document | Guiding Architecture Principles |
| Version | 1.0 |
| Status | Draft |
| Repository | farhanmae/gotripzee_docs |
| Related Documents | [Current System Assessment](./02-current-system-assessment.md), [Business Process Analysis (AS-IS)](./03-business-process-analysis-as-is.md), [Target Operating Model](./04-target-operating-model.md), [Domain Model](./06-domain-model.md) |

## 1. Purpose

This document defines the non-negotiable architectural principles that will guide all future design, development, integration, and migration decisions for the GoTripzee modernization program.

These principles ensure the solution remains business-aligned, composable, upgrade-safe, and scalable while extending ERPNext instead of competing with it.

## 2. Why This Document Exists

The current platform has evolved organically over time. In such systems, architectural decisions can become inconsistent unless a stable set of principles is explicitly documented.

This document serves as the architectural constitution of the program. Every major requirement, design choice, and implementation decision should be evaluated against these principles.

## 3. Core Architectural Philosophy

GoTripzee should be treated as a **travel business platform**, not as a collection of isolated booking modules or a Drupal-to-Frappe technical conversion.

The modernization must preserve the business value already present in the existing platform while redesigning the implementation into a structured, reusable, domain-driven architecture.

## 4. Guiding Principles

### Principle 1 — ERPNext is the Enterprise System of Record

ERPNext shall remain the authoritative source for enterprise masters and financial records.

ERPNext should own:

- Company
- Customer
- Supplier
- User
- Employee
- Contact
- Address
- Accounts
- Invoices
- Payments
- Price Lists
- Tax rules
- Core CRM entities
- Role and permission governance

The travel platform should extend these entities where needed, but it should not duplicate them.

### Principle 2 — No ERPNext Core Modifications

The solution shall not modify ERPNext core code.

All custom behavior must be implemented through supported extension mechanisms such as:

- Custom Frappe app
- Custom DocTypes
- Hooks
- Property setters
- Workflows
- Server scripts
- Fixtures
- Background jobs
- REST APIs

This preserves upgrade safety and reduces future maintenance risk.

### Principle 3 — Business First, Not Drupal First

The target design should model business concepts directly rather than mirroring legacy Drupal entities or module boundaries.

The correct question is not, “What did Drupal do?”
It is, “What is the real business capability?”

### Principle 4 — Composable Travel Products

Travel services shall be modelled as reusable products that can be sold independently or composed into packages.

A hotel, transfer, activity, or cab should be reusable across multiple commercial offers.

Packages should reference existing products rather than duplicating them.

### Principle 5 — Generic Before Specific

Common workflows should be implemented once and reused across product types.

Examples:

- Booking
- Reservation
- Allocation
- Payment tracking
- Notifications
- Document handling
- Approval workflows

Product-specific behavior should extend generic services rather than introduce duplicate implementations.

### Principle 6 — Separate Commercial and Operational Concerns

A customer booking is not the same as an operational assignment.

The solution shall distinguish between:

- Booking: the commercial commitment
- Reservation: the service commitment
- Allocation: the physical operational assignment

This separation allows operations to adjust resources without rewriting the customer’s commercial history.

### Principle 7 — Shared Inventory Across Selling Paths

Inventory should belong to the underlying resource or product, not to the package wrapper that sells it.

If a stay is sold directly, and the same stay is also included inside a package, both sales paths must block the same underlying inventory.

This prevents duplicate inventory, overbooking, and manual synchronization issues.

### Principle 8 — Configuration Over Hard-Coding

Business behavior should be driven by configuration wherever possible.

Examples:

- Company-specific product visibility
- Product offering enablement
- Pricing rules
- Cancellation policies
- Inventory rules
- Workflow routing
- Notification behavior

Business variation should usually be configuration, not code.

### Principle 9 — Multi-Company by Design

The platform must support multiple companies or brands from a single codebase.

Each company may have:

- Different product enablement
- Different branding
- Different pricing rules
- Different taxes
- Different operational policies

This should be handled as a first-class design concern, not as an afterthought.

### Principle 10 — Single Source of Truth

Every business entity must have one clear owner.

| Entity | System Owner |
|---|---|
| Company | ERPNext |
| Customer | ERPNext |
| Supplier | ERPNext |
| Contact | ERPNext |
| Address | ERPNext |
| Finance | ERPNext |
| Travel Product | Travel platform |
| Product Offering | Travel platform |
| Booking | Travel platform |
| Reservation | Travel platform |
| Allocation | Travel platform |
| Itinerary | Travel platform |
| Operations | Travel platform |

### Principle 11 — API-First Design

Core business capabilities should be exposed through stable APIs.

The React frontend, future partner portals, mobile applications, and third-party integrations should all consume the same service layer.

Business logic should not be embedded inside UI components.

### Principle 12 — Event-Driven Workflow Awareness

Important business events should be captured and reused across the platform.

Examples:

- Enquiry Created
- Quotation Generated
- Booking Confirmed
- Payment Received
- Reservation Created
- Inventory Allocated
- Booking Cancelled
- Trip Completed

This enables automation, notifications, auditing, analytics, and future AI workflows.

### Principle 13 — Security by Design

Security must be built into the platform architecture.

The solution should support:

- Role-based access control
- Company-aware permissions
- Audit logging
- Secure authentication
- API authorization
- Secret management
- Data access governance

Security should not depend only on client-side controls.

### Principle 14 — AI-Ready Data and Services

The platform should be designed so AI capabilities can be added later without redesigning the core business model.

This requires structured data, consistent service boundaries, and traceable business events.

Potential AI use cases include:

- Itinerary generation
- Travel recommendations
- Customer support assistance
- Pricing suggestions
- Operational planning support
- Sales follow-up automation
- Knowledge search

### Principle 15 — Build for Long-Term Evolution

The solution should be designed to last well beyond the current migration.

It must be capable of supporting future expansion into:

- Marketplace operations
- Supplier portals
- Corporate travel
- B2B channels
- White-label deployments
- New product types
- AI-driven automation

## 5. Decision Evaluation Checklist

Every significant design or implementation decision should be checked against the following questions:

1. Does this duplicate an ERPNext capability?
2. Is this a real business concept or a technical workaround?
3. Can this capability be reused across product types?
4. Is this configurable rather than hard-coded?
5. Does this preserve upgrade safety?
6. Does this support multi-company deployment?
7. Does this separate commercial and operational concerns?
8. Can this be extended without redesign?
9. Does this align with the composable product model?
10. Will this still be sensible as the business expands?

If the answer to any of these is “no”, the design should be revisited.

## 6. Implications for Delivery

These principles affect every downstream deliverable:

- Current System Assessment
- Business Process Analysis (AS-IS)
- Target Operating Model
- Domain Model
- Business Requirements Document
- Solution Architecture
- Database Design
- API Specification
- UX/UI Design
- Migration Strategy
- Testing Strategy
- Deployment Strategy

## 7. Summary

The guiding principles establish the rules for how the platform must be designed and evolved. They ensure that the modernization effort is not treated as a simple rewrite, but as a long-term architecture program that preserves business value, improves maintainability, and creates a foundation for growth.

## 8. Traceability to Next Documents

This document feeds into:

- [Domain Model](./06-domain-model.md)
- [Business Requirements Document](./07-business-requirements-document.md)
- [Solution Architecture](./08-solution-architecture.md)
