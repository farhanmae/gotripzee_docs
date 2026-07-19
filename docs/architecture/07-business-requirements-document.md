# Business Requirements Document

## Document Control

| Field | Value |
|---|---|
| Document | Business Requirements Document |
| Version | 1.0 |
| Status | Draft |
| Repository | farhanmae/gotripzee_docs |
| Related Documents | [Current System Assessment](./02-current-system-assessment.md), [Business Process Analysis (AS-IS)](./03-business-process-analysis-as-is.md), [Target Operating Model](./04-target-operating-model.md), [Guiding Architecture Principles](./05-guiding-architecture-principles.md), [Domain Model](./06-domain-model.md) |

## 1. Purpose

This document translates the business analysis and domain model into a structured set of business requirements for the modernized GoTripzee platform. It focuses on what the business needs the system to do, not how the system should technically implement those needs.

## 2. Business Objective

GoTripzee requires a modern travel business platform that preserves the current commercial and operational capabilities of the existing system while improving reuse, composability, ERPNext alignment, maintainability, and long-term scalability.

## 3. Business Goals

1. Preserve all commercially valuable current capabilities.
2. Reuse ERPNext for enterprise masters and finance.
3. Support reusable and composable travel products.
4. Separate booking from reservation and allocation.
5. Improve inventory handling across direct and bundled sales.
6. Support company-specific product enablement.
7. Enable future supplier and marketplace participation.
8. Improve reporting, governance, and operational control.
9. Create a strong foundation for future AI-assisted features.

## 4. Scope

### In Scope

- travel product management
- product offerings
- company-wise product enablement
- packages and component-based composition
- enquiries and lead capture
- quotation generation
- booking management
- reservation management
- inventory allocation
- stay and transport fulfilment
- payments and status tracking
- customer communication
- cancellation and refund handling
- reporting and analytics
- ERPNext integration

### Out of Scope for This Document

- low-level database schema
- UI component design
- API route definitions
- deployment engineering
- code implementation details

## 5. Business Domain Requirements

### 5.1 Travel Product Management

#### Requirement
The system shall allow administrators to create and manage reusable travel products.

#### Business Need
The business needs to sell different kinds of travel services from one platform without duplicating logic for each sales path.

#### Key Capabilities

- create products
- categorize by product type
- publish or unpublish products
- attach SEO and marketing content
- control visibility by company
- support multiple offerings per product

#### Priority
High

### 5.2 Product Offerings

#### Requirement
The system shall support multiple offerings per product such as Budget, Standard, Premium, and Luxury.

#### Business Need
Packages and weekend trips may have different commercial versions with different inclusions and prices.

#### Key Capabilities

- variant pricing
- variant inclusions/exclusions
- company-specific enablement
- variant-specific policies
- variant-specific availability windows

#### Priority
High

### 5.3 Package Composition

#### Requirement
The system shall allow packages to be composed from existing travel products.

#### Business Need
Packages may include already listed stays, transfers, activities, meals, or other services that should be reusable and not duplicated.

#### Key Capabilities

- reference existing products in packages
- define ordered package components
- support package-level itinerary structure
- reuse stays and other services across standalone and package sales

#### Priority
High

### 5.4 Multi-Company Product Enablement

#### Requirement
The system shall allow products to be enabled or disabled per company.

#### Business Need
The same codebase should support different companies or brands.

#### Key Capabilities

- company-level product visibility
- company-level pricing configuration
- company-level branding and commercial rules
- reuse the same product model across multiple businesses

#### Priority
High

### 5.5 Enquiry and Lead Management

#### Requirement
The system shall capture enquiries and convert them into sales opportunities.

#### Business Need
The business needs an auditable path from marketing interest to quotation and booking.

#### Key Capabilities

- enquiry capture
- customer requirement capture
- sales follow-up
- lead qualification
- enquiry-to-booking traceability

#### Priority
High

### 5.6 Quotation Management

#### Requirement
The system shall support quotation preparation and revision before booking.

#### Business Need
The sales team needs a structured way to respond to customer requirements and pricing discussions.

#### Key Capabilities

- quotation creation
- quotation revision
- offer comparison
- validity periods
- approval or negotiation support

#### Priority
High

### 5.7 Booking Management

#### Requirement
The system shall manage bookings as the commercial commitment between customer and business.

#### Business Need
Booking is the core transaction that drives payment, fulfilment, and post-booking service delivery.

#### Key Capabilities

- booking creation
- booking status tracking
- traveler association
- payment linkage
- commercial history preservation

#### Priority
High

### 5.8 Reservation Management

#### Requirement
The system shall create reservations to represent capacity commitment for a booking.

#### Business Need
The business needs a distinct layer between booking and actual operational assignment.

#### Key Capabilities

- reservation creation
- reservation status tracking
- reservation quantity tracking
- reservation-level inventory hold

#### Priority
High

### 5.9 Inventory Allocation

#### Requirement
The system shall allocate actual operational resources against reservations.

#### Business Need
The operations team needs to assign specific resources after the commercial booking has been confirmed.

#### Key Capabilities

- room allocation
- vehicle allocation
- activity allocation
- departure allocation
- reallocation support
- inventory blocking

#### Priority
High

### 5.10 Stay Inventory Blocking

#### Requirement
The system shall automatically block stay inventory when a listed stay is added to a package booking.

#### Business Need
If a package uses a listed stay, that stay’s inventory must be reduced or blocked exactly as if it had been sold directly.

#### Key Capabilities

- shared inventory pool for direct and package sales
- automatic inventory blocking on assignment
- availability consistency across all sales paths
- operational override and reassignment handling

#### Priority
Critical

### 5.11 Pricing Management

#### Requirement
The system shall support structured pricing for products and offerings.

#### Business Need
The business needs reusable pricing that supports offerings, seasons, company rules, and product-specific commercial logic.

#### Key Capabilities

- base pricing
- offering pricing
- seasonal pricing
- company pricing
- package pricing
- configurable pricing rules

#### Priority
High

### 5.12 Payments and Accounting

#### Requirement
The system shall integrate with payment and accounting flows through ERPNext.

#### Business Need
The business requires reliable payment tracking, invoicing, reconciliation, and accounting integrity.

#### Key Capabilities

- payment capture
- payment status tracking
- invoice generation
- refund tracking
- ERPNext finance integration

#### Priority
High

### 5.13 Customer Communication

#### Requirement
The system shall support communication for enquiry, quotation, booking, and fulfilment events.

#### Business Need
Customers require timely and traceable communication throughout the lifecycle.

#### Key Capabilities

- email notifications
- SMS notifications
- status updates
- booking confirmation messages
- operational communication

#### Priority
Medium to High

### 5.14 Cancellation and Refunds

#### Requirement
The system shall support cancellation, release of reservations, and refund handling.

#### Business Need
Travel bookings often change and require a controlled cancellation and refund process.

#### Key Capabilities

- cancellation workflow
- inventory release
- refund calculation support
- partial or full cancellation handling

#### Priority
High

### 5.15 Reporting and Analytics

#### Requirement
The system shall provide reporting across sales, bookings, inventory, fulfilment, and profitability.

#### Business Need
The business needs visibility into performance, bottlenecks, and product economics.

#### Key Capabilities

- booking reports
- product reports
- occupancy / utilization reports
- company-wise analysis
- revenue reports
- operational progress reports

#### Priority
High

## 6. Non-Functional Requirements

### 6.1 Maintainability

The solution shall be maintainable through modular design, clear ownership boundaries, and upgrade-safe extension patterns.

### 6.2 Scalability

The solution shall support growth in product count, booking volume, and company count.

### 6.3 Security

The solution shall enforce role-based access, company-aware access, secure authentication, and auditability.

### 6.4 Availability

The platform shall support business operations with high availability expectations appropriate for a customer-facing commercial system.

### 6.5 Performance

The system shall provide fast discovery, quotation, and booking interactions for the customer and sales teams.

### 6.6 Extensibility

The solution shall support future product types, marketplace participation, AI assistance, and new integration channels without redesigning the core model.

## 7. Functional Requirement Summary

| Area | Requirement Summary | Priority |
|---|---|---|
| Travel products | Manage reusable products and offerings | High |
| Packages | Compose packages from existing products | High |
| Multi-company | Enable or disable products by company | High |
| Enquiries | Capture and track customer interest | High |
| Quotations | Prepare, revise, and track offers | High |
| Bookings | Manage customer commitments | High |
| Reservations | Hold capacity for bookings | High |
| Allocations | Assign real operational resources | High |
| Stay inventory | Block shared inventory correctly | Critical |
| Pricing | Govern base and travel pricing rules | High |
| Payments | Integrate with ERPNext finance | High |
| Communication | Notify customers and staff | Medium/High |
| Reporting | Deliver operational and commercial insight | High |
| Cancellations | Support change and refund workflows | High |

## 8. ERPNext Integration Requirements

### Requirement
The system shall extend ERPNext rather than replacing it.

### Implications

- Customer should remain ERPNext-owned.
- Supplier should remain ERPNext-owned.
- Contacts, addresses, accounts, and payments should reuse ERPNext capabilities.
- The travel platform should add only travel-specific logic.
- No modification to ERPNext core is allowed.

## 9. Business Rules

1. A product may be enabled for one or more companies.
2. A product may have multiple offerings.
3. A package may include listed stays and other reusable services.
4. A booking may generate one or many reservations.
5. Reservations may generate one or many allocations.
6. Inventory must be shared across direct sales and package sales.
7. Stay inventory must be blocked when allocated to a package booking.
8. Commercial booking status must be preserved even when operational allocations change.
9. ERPNext remains the enterprise source of truth.
10. Travel-specific business logic should remain within the travel platform.

## 10. Acceptance Criteria

The modernization will meet business requirements when:

- travel products are reusable and company-aware
- packages can include existing listed stays and other services
- stay inventory is blocked automatically when allocated
- booking, reservation, and allocation are separated
- ERPNext owns the enterprise masters and finance
- reporting and communications support the full lifecycle
- the platform remains upgrade-safe and maintainable

## 11. Traceability to Solution Documents

This BRD feeds into:

- [Solution Architecture](./08-solution-architecture.md)
- [Database Design](./09-database-design.md)
- [API Specification](./10-api-specification.md)
- [Frontend Architecture](./11-frontend-architecture.md)
- [Migration Strategy](./16-migration-strategy.md)
