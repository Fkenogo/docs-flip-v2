# DOCSFLIP-BIZ-001 — Business Model

**Document ID:** DOCSFLIP-BIZ-001  
**Title:** Business Model  
**Version:** 0.4 (Loop 3 — Architectural Integration)  
**Status:** Active Draft  
**Maturity:** L2 — Expanded  
**Repository Path:** `docs/01-product-foundation/`  
**Authority:** Founder  
**Parent Documents:** DOCSFLIP-MP-001, DOCSFLIP-PA-001, DOCSFLIP-CAP-001

---

# 1. Purpose

This document defines how Docsflip creates, delivers and captures value as a business. It translates the Product Foundation (CON-001) and the Capability Framework (CAP-001 through CAP-005) into a structured business model.

It intentionally stops short of describing commercial mechanics such as credits, pricing, payment flows and publication charging. Those belong in **DOCSFLIP-COM-001 — Commercial Architecture**.

---

# 2. Document Responsibility Statement

BIZ-001 owns the business strategy of Docsflip. It defines the value model, market model, and operating model at the business level.

**BIZ-001 owns:**

- Business purpose and rationale (derived from CON-001).
- Value creation, delivery, and capture logic.
- Customer segment definition and market geography.
- Customer relationship strategy and channel architecture.
- Business capabilities, resources, partnerships, and cost structure.
- Revenue stream definition.
- Strategic differentiation.

**BIZ-001 does not own:**

- Product identity, philosophy, or principles → CON-001.
- Architecture domains or capability definitions → PA-001 and CAP-001.
- Commercial mechanics (credits, pricing, payments) → COM-001.
- User personas or stakeholder analysis → USR-001.
- User journeys → JNY-001.
- Technical architecture or implementation → ARC-001.

---

# Part 1 — Value Model

## 3. Business Purpose

Docsflip exists to make professional digital publishing accessible, transparent and affordable for African organisations of every size.

The business purpose is derived directly from the Product Foundation (CON-001): to remove unnecessary barriers between creating knowledge and publishing it digitally. Docsflip serves organisations that produce valuable PDF content — reports, catalogues, magazines, manuals, research — and want to publish it professionally without committing to subscription obligations they do not need.

The business operates on a fundamental belief: publishing outcomes define value. The platform generates revenue when customers publish, not when they maintain accounts. This aligns the business's commercial interests with customer value — Docsflip succeeds when its customers successfully publish.

**Constitutional basis:** CON-001 §4 (Vision), §5 (Mission), §6 (Product Purpose), PH-001 (Publishing Outcomes Define Value).

---

## 4. Value Creation

Docsflip creates value by enabling organisations to transform static PDF documents into interactive, shareable digital publications.

**How value is created:**

### Publishing Transformation

The core value creation mechanism is the conversion of PDF documents into professional digital flipbook publications. A document that was previously a static file becomes an interactive, mobile-responsive, shareable publication. This transformation enables organisations to present their content in formats that engage readers and reflect professional quality.

**Capability owner:** Publications (CAP-001 §2, PA-001 §4.3).

### Barrier Reduction

Docsflip removes the barriers that prevent occasional publishers from accessing digital publishing. By eliminating mandatory subscriptions, the platform allows organisations to publish when they need to — whether once a year or every day. This creates value for segments that existing platforms exclude: NGOs publishing annual reports, government institutions distributing policy documents, independent publishers releasing occasional catalogues.

**Constitutional basis:** CON-001 PH-003 (Access Should Not Require Unnecessary Commitment).

### Organisational Enablement

The platform enables organisations to manage publishing as a team activity. Workspaces, role-based permissions, approval workflows, and consolidated billing allow organisations to integrate publishing into their existing operational structures rather than treating it as an individual activity.

**Capability owner:** Organisations (CAP-001 §2, PA-001 §4.2).

### African Market Relevance

By designing for African payment methods, procurement processes, and publishing patterns from the start, Docsflip creates value that international platforms cannot easily replicate. African organisations encounter a platform that understands their payment realities, their organisational structures, and their publishing needs.

**Constitutional basis:** CON-001 PH-006 (Africa Is a Design Assumption), PP-009 (Market-Aware).

### Transparency as Value

The platform's commitment to transparent pricing — showing costs before commitment, maintaining an immutable credit ledger, never silently consuming credits — creates trust value. Customers know what they will pay, what they will receive, and what remains.

**Constitutional basis:** CON-001 PH-002 (Transparency Is a Product Feature), PP-003 (Transparency by Design).

---

## 5. Value Delivery

Value is delivered to customers through multiple channels and mechanisms designed for accessibility, reliability, and organisational fit.

### Self-Service Publishing Platform

The primary delivery mechanism is the Docsflip web platform. Customers create accounts, upload PDFs, preview publications, approve costs, publish, and manage their publications through a self-service interface. The publishing flow is designed to be understood on first use — no training, documentation, or support intervention should be required for the core publishing transaction.

**Capability owner:** Publications (Creation), Identity.

### Cloud-Hosted Publications

Published documents are hosted on Docsflip infrastructure with defined hosting durations, renewal mechanisms, and clear lifecycle states. Customers receive shareable links, embed codes, and QR codes for distribution. Hosting is managed — customers do not need to maintain infrastructure.

**Capability owner:** Publications (Management), Publications (Distribution).

### Organisation Workspaces

For organisational customers, value is delivered through managed workspaces that support teams, roles, permissions, and collaborative publishing workflows. Organisation administrators can manage members, allocate publishing capacity, and monitor organisational publishing activity.

**Capability owner:** Organisations (CAP-002, PA-001 §4.2).

### Offline and Self-Hosted Outputs

Customers who require independence from Docsflip hosting can purchase self-hosted interactive publication packages. These deliver the complete publication — HTML, JavaScript, assets, viewer — for the customer to host independently.

**Capability owner:** Publications (Distribution), Commercial (Publication Outputs).

### Publication Analytics

Customers receive publication performance data — views, readership, engagement metrics — enabling them to measure the impact of their published content.

**Capability owner:** Analytics (CAP-001 §2, PA-001 §5.2).

### Secure Sharing and Access

Publications are distributed through permanent shareable links, website embeds, and QR codes with access control policies. Customers control who can view their publications and how they are distributed.

**Capability owner:** Publications (Distribution), Reader Experience.

---

## 6. Value Capture

Docsflip captures value through a pay-as-you-publish commercial model. Revenue is generated when customers publish and consume publishing services.

### Revenue Model

**Pay-Per-Publication (Primary)**
The primary revenue mechanism is per-publication charging. Customers purchase Docsflip Credits in bundles and consume them when they create publication outputs. Revenue is recognised at the point of credit consumption — when a customer publishes a document, adds a publication enhancement, or renews hosting.

**Capability owner:** Commercial (CAP-001 §2, PA-001 §4.4).

**Credit Bundle Purchases**
Customers pre-purchase publishing capacity through credit bundles. Bundle sizes are designed to serve different publishing frequencies: small bundles for occasional publishers, larger bundles for regular publishers, and allocated credit pools for organisational subscriptions. Purchased credits do not expire merely because time has passed.

**Constitutional basis:** CON-001 PH-003, PP-002 (Pay for Value Delivered).

**Organisation Subscriptions**
Larger organisations may subscribe to managed workspaces with monthly or annual credit allocations, consolidated billing, and organisational administration features. Subscriptions provide predictable revenue while maintaining the credit-based consumption model — organisations still see how credits are consumed by publication, team member, or department.

**Enterprise and Institutional Arrangements**
Large publishers, institutions, and public bodies may negotiate custom pricing, volume commitments, invoicing, and tailored service terms. These arrangements provide high-value, long-term revenue relationships.

### Value Capture Principles

- Revenue aligns with customer value — Docsflip earns when customers publish.
- Commercial mechanics remain transparent — every cost is visible before commitment.
- The detailed commercial engine — credits, publication outputs, pricing, bundles, and payment rules — is defined separately in COM-001 (CAP-001 §2, COM-001).

---

## 7. Business Capability Traceability

Every business capability traces to a PA-001 domain, which in turn traces to a CAP-001 Level 1 capability.

| Business Capability | PA-001 Domain (§) | CAP-001 Capability     | CAP-002 Sub-capabilities                                                        |
| ------------------- | ----------------- | ---------------------- | ------------------------------------------------------------------------------- |
| Publications        | PA-001 §4.3       | Publications (L1)      | Creation, Management, Distribution                                              |
| Organisations       | PA-001 §4.2       | Organisations (L1)     | Org Management, Workspace, Membership, Roles, Invitations, Collaboration        |
| Commercial          | PA-001 §4.4       | Commercial (L1)        | Wallet, Credits, Payments, Entitlements, Publication Outputs                    |
| Identity            | PA-001 §4.1       | Identity (L1)          | Registration, Authentication, Profile, Account Lifecycle, Preferences           |
| Reader Experience   | PA-001 §5.1       | Reader Experience (L1) | Reading, Navigation, Search, Accessibility, Reader Preferences                  |
| Analytics           | PA-001 §5.2       | Analytics (L1)         | Publication Metrics, Reader Behaviour, Publisher Insights, Commercial Reporting |

**Primary business asset:** Publication (CAP-004). All other business assets (User, Organisation, Workspace, Wallet, Credit, Payment, Reader Session, Analytics Event) exist to create, govern, experience, commercialise, or measure publications (CAP-004).

---

# Part 2 — Market Model

## 8. Customer Segments

Docsflip serves organisations and individuals who create PDF-based content and want to publish it digitally. Customer segments are defined by their publishing patterns, organisational context, and commercial preferences. Detailed user personas for each segment belong in USR-001.

### Primary Segments

**Publishing Houses**
Magazine publishers, newspaper digitisation, journal publishers, and recurring edition producers. Publishing houses represent the highest-volume segment. They require recurring publishing workflows, volume credit pricing, publication libraries, and long-term publication management. Organisation subscriptions with allocated credit pools are the natural commercial fit.

**Corporate Organisations**
Businesses producing annual reports, company profiles, product catalogues, sustainability reports, investor publications, internal magazines, and event programmes. Corporate publishing is typically periodic — quarterly, annual, or event-driven. Credit bundle purchases and organisation workspaces with approval workflows serve this segment.

**NGOs and Development Organisations**
Organisations publishing programme reports, evaluation reports, impact reports, policy briefs, research publications, newsletters, and training materials. This segment is characterised by project-based publishing cycles, donor reporting requirements, and sensitivity to cost. Pay-per-publication with low entry cost is essential. Organisation workspaces with team collaboration are valuable.

**Government and Public Institutions**
Ministries, agencies, and public bodies publishing strategic plans, statistical reports, policies, public consultation documents, and public information materials. This segment requires procurement-compatible payment (invoicing, purchase orders), formal approval workflows, and long-term publication hosting. Enterprise arrangements are appropriate.

**Educational Institutions**
Universities, research centres, and training organisations publishing research outputs, journals, course materials, and institutional publications. This segment values accessibility, long-term archival, and institutional branding.

### Secondary Segments

**Independent Publishers and Creators**
Individual creators publishing magazines, digital books, portfolios, catalogues, and event publications. They need simple, fast publishing with minimal administration. Small credit bundles and pay-per-publication are the natural fit.

**Agencies and Service Providers**
Communications agencies, design firms, and marketing service providers who publish on behalf of clients. While Docsflip is not an agency-first platform, agencies represent a channel to market rather than a primary customer segment.

**Cross-reference:** Detailed user personas, needs analysis, and stakeholder mapping → USR-001.

---

## 9. Customer Relationships

Docsflip builds and maintains customer relationships through transparency, reliability, and respect for customer autonomy.

### Relationship Principles

**Transparency-Based Trust**
The commercial relationship is founded on transparency. Costs are visible before commitment. Every credit consumption is recorded in an immutable ledger. Hosting status, renewal dates, and publication states are always visible. Customers are never surprised by charges, limitations, or platform behaviours.

**Self-Service with Support**
The platform is designed for self-service — customers should be able to publish without assistance. Support is available for exceptions, not as a requirement for normal operation. As the platform matures, support may tier from self-service documentation through community support to dedicated account management for enterprise customers.

**Low-Commitment Engagement**
Customers can publish a single document, pay for it, and leave. They can return months later and publish again. The platform does not penalise inactivity or require ongoing commitment. This builds relationships with occasional publishers who would be excluded by subscription-only models.

**Organisational Relationship Management**
For organisational customers, relationships are managed at the workspace level. Organisation administrators control membership, permissions, and commercial settings. The platform supports the organisation's internal governance rather than imposing its own.

**Long-Term Publishing Partnership**
For regular publishers, Docsflip aims to become a trusted publishing partner. Reliable hosting, predictable costs, publication lifecycle management, and performance analytics build long-term retention. The relationship deepens as customers publish more and integrate Docsflip into their publishing workflows.

---

## 10. Channels

Customers discover, evaluate, and access Docsflip through multiple channels.

### Direct Web Platform

The primary channel is the Docsflip web application. Customers create accounts, purchase credits, publish documents, and manage publications directly through the platform. This is the lowest-cost, highest-margin channel.

### Digital Marketing and Content

Organic search, content marketing (publishing guides, case studies), and social media presence drive discovery. Docsflip's positioning as "Africa's pay-as-you-publish platform" provides a clear, searchable value proposition.

### Partner Organisations

Publishing associations, business networks, NGO coordination bodies, and government digital transformation programmes provide referral and distribution channels. Partnerships may include co-branded landing pages, referral arrangements, or integrated service offerings.

### Strategic Partnerships

Payment providers (mobile money platforms, card processors, invoicing services) serve as both infrastructure and discovery channels. Technology partners (PDF tooling, content management systems) may integrate Docsflip publishing into their workflows.

### Direct Outreach

For enterprise and institutional customers, direct relationship development — demonstrations, proposals, procurement engagement — is appropriate. This channel serves government ministries, large publishing houses, and institutional customers with formal procurement requirements.

---

## 11. Market Geography

Docsflip is designed for Africa and launched from East Africa, with progressive continental expansion.

### Primary Market: Africa

Docsflip's product, commercial model, payment architecture, and market assumptions are built for African organisations. This is not a "launch in developed markets, expand to Africa later" strategy. Africa is the design centre.

**Constitutional basis:** CON-001 §1.4, §2, PH-006, PP-009.

### Initial Launch: East Africa

East Africa provides a concentrated launch market with established mobile money infrastructure (M-PESA and equivalents), growing digital publishing demand, and a mix of organisational types (NGOs, corporate, government, publishing houses). Launch countries will be selected based on payment infrastructure readiness, regulatory environment, and market demand.

### Expansion Model

Expansion is progressive and country-configurable. As Docsflip adds country support, the platform enables country-specific payment methods, currencies, tax configurations, and localisation without architectural redesign. This allows the business to expand at the pace of payment infrastructure and market readiness rather than being constrained by platform limitations.

### Market Sizing

The addressable market includes organisations across Africa that produce PDF-based content and want to publish it digitally. This spans publishing houses, corporate organisations, NGOs and development organisations, government institutions, educational organisations, and independent publishers. The market is served by a small number of international platforms that do not optimise for African payment realities or occasional publishing patterns.

---

# Part 3 — Operating Model

## 12. Key Capabilities

Docsflip's business capabilities are the activities the organisation must perform to deliver its value proposition. Each capability maps to a domain defined in the Product Architecture (PA-001) and the Capability Framework (CAP-001).

### Publications

The core capability — converting PDF documents into interactive digital publications, hosting them, managing their lifecycle, and enabling their distribution. Publications capabilities include document ingestion, validation, conversion, preview, publishing, hosting, metadata management, lifecycle state management, sharing, embedding, and archival. This is the capability that directly creates customer value.

**PA-001:** §4.3 | **CAP-001:** Publications (L1) | **CAP-002:** Creation, Management, Distribution

### Organisations

Enabling organisational customers to manage publishing as a team activity. Organisation capabilities include workspace creation, team management, membership, role-based permissions, invitation workflows, collaboration settings, and organisational branding. This capability transforms Docsflip from an individual tool into an organisational platform.

**PA-001:** §4.2 | **CAP-001:** Organisations (L1) | **CAP-002:** Org Management, Workspace, Membership, Roles, Invitations, Collaboration

### Analytics

Measuring publication performance and providing business intelligence. Analytics capabilities include publication metrics (views, readership, engagement), reader behaviour tracking, publisher insights, commercial reporting, and geographic distribution data. This capability enables customers to measure the impact of their publishing and enables Docsflip to understand market behaviour.

**PA-001:** §5.2 | **CAP-001:** Analytics (L1) | **CAP-002:** Publication Metrics, Reader Behaviour, Publisher Insights, Commercial Reporting

### Identity

User acquisition, account management, authentication, and credential lifecycle. Identity capabilities include registration, login, profile management, account recovery, and personal preferences. This capability is the entry point for all customer relationships and enables trust through secure, privacy-respecting identity management.

**PA-001:** §4.1 | **CAP-001:** Identity (L1) | **CAP-002:** Registration, Authentication, Profile, Account Lifecycle, Preferences

### Commercial

The economic engine — credits, wallets, payments, entitlements, and publication output monetisation. Commercial capabilities include wallet management, credit purchase, credit consumption, cost preview, entitlement management, and transaction history. This capability translates publishing activity into business revenue.

**PA-001:** §4.4 | **CAP-001:** Commercial (L1) | **CAP-002:** Wallet, Credits, Payments, Entitlements, Publication Outputs

### Reader Experience

Publication consumption — reading, navigation, accessibility, and reader interaction. Reader Experience capabilities include the flipbook viewer, page navigation, search within publication, mobile-responsive viewing, and accessibility features. This capability delivers value to publication readers and drives audience growth for publishers.

**PA-001:** §5.1 | **CAP-001:** Reader Experience (L1) | **CAP-002:** Reading, Navigation, Search, Accessibility, Reader Preferences

> **Note:** Customer support and platform administration are operational concerns deferred to Solution Architecture (ARC-001). They are not business capabilities in the architectural sense (CAP-001 §5).

---

## 13. Key Resources

The assets required to deliver the business model.

### Technology Platform

The Docsflip software platform — including the web application, PDF conversion engine, publication viewer, hosting infrastructure, payment integration layer, and analytics pipeline — is the foundational technological resource.

### People

The team required to build, operate, and grow Docsflip. Key roles include product management, software engineering, user experience design, commercial operations, customer support, marketing, and business development. Engineering governance is provided through the Founder Engineering Framework (FEF).

### Brand and Reputation

Docsflip's positioning as "Africa's pay-as-you-publish platform" and its commitment to transparency, simplicity, and African market relevance are intangible assets that differentiate the business from international competitors.

### Payment Infrastructure Relationships

Partnerships with payment providers (mobile money platforms, card processors, invoicing services) are critical infrastructure resources. The platform's payment abstraction layer allows provider relationships to evolve without architectural disruption.

### Customer Base and Publication Portfolio

As customers publish, the accumulated portfolio of hosted publications, publisher relationships, and usage data becomes a strategic resource for retention, product improvement, and market intelligence.

---

## 14. Key Partnerships

External relationships that enable or enhance the business model.

### Payment Providers

Mobile money platforms (M-PESA and equivalents), card payment processors, bank payment services, and invoicing platforms. These partnerships enable the African payment support that is central to Docsflip's value proposition. Pesapal may be assessed as an initial partner due to its African payment integrations.

### Technology Infrastructure Providers

Cloud hosting providers, CDN services, PDF processing tooling, and analytics infrastructure vendors. These partnerships provide the technical foundation without requiring Docsflip to build commodity infrastructure.

### Publishing and Content Partners

Organisations that integrate Docsflip publishing into their content workflows — content management systems, document preparation tools, and publishing platforms. These partnerships extend Docsflip's reach into existing customer workflows.

### Channel Partners

Publishing associations, business networks, NGO coordination bodies, and government digital transformation programmes that refer customers, co-market, or integrate Docsflip into their service offerings.

### Strategic Resellers and Agencies

Communications agencies, design firms, and marketing service providers who publish on behalf of clients. While Docsflip is not an agency-first platform, agencies represent a scalable channel for customer acquisition.

---

## 15. Cost Structure

The costs incurred to operate the business model.

### Platform Development and Maintenance

Software engineering, product management, design, and quality assurance. These are the primary ongoing costs. The Founder Engineering Framework (FEF) provides governance that should reduce waste and rework.

### Cloud Infrastructure

Hosting, storage, content delivery, PDF processing compute, and analytics infrastructure. Infrastructure costs scale with publication volume and reader traffic. The per-publication cost must remain below the revenue generated per publication.

### Payment Processing

Transaction fees from payment providers, currency conversion costs, and payment gateway charges. These are variable costs that scale with revenue. African payment methods may have different fee structures than international card networks.

### Customer Acquisition and Marketing

Digital marketing, content production, partnership development, and direct outreach. Customer acquisition cost must be recoverable within a reasonable number of publication transactions per customer.

### Operations and Support

Customer support, platform operations, compliance, legal, and administration. These are largely fixed costs that become proportionally smaller as the business scales.

### Cost Structure Principles

- Variable costs (infrastructure, payment processing) should scale proportionally with revenue.
- Fixed costs (development, operations) should be managed for efficiency as the business grows.
- The per-publication margin — revenue per publication minus variable costs — must be positive at the lowest credit bundle level.

---

## 16. Revenue Streams

How the business generates revenue from each customer segment. The detailed commercial rules, pricing, credit mechanics, and payment strategy are defined in COM-001.

### Credit Bundle Purchases (All Segments)

Individual customers purchase Docsflip Credits in bundles. Bundle sizes range from introductory low-cost bundles (enabling the "from as little as $1" proposition) through regular bundles for frequent publishers to large bundles for volume publishers. Credits are consumed on publication, creating a direct link between customer value and business revenue.

### Organisation Subscriptions (Publishing Houses, Corporate, NGO, Government)

Organisations subscribe to managed workspaces with monthly or annual credit allocations, consolidated billing, and organisational features. Subscriptions provide recurring revenue while maintaining the transparent, credit-based consumption model.

### Publication Output Add-Ons (All Segments)

Additional revenue is generated from publication enhancements: extra pages beyond the base allowance, branding removal, custom logo placement, website embed generation, offline interactive packages, self-hosted publication packages, hosting renewal, and advanced analytics.

### Enterprise Arrangements (Government, Large Publishers, Institutions)

Custom pricing, volume commitments, invoicing, and negotiated service terms for large customers with formal procurement requirements. These arrangements provide high-value, long-term revenue with lower transaction frequency.

### Revenue Principles

- The "from as little as $1" proposition communicates accessibility without requiring every transaction to be $1.
- Purchased credits do not expire — unused credits represent deferred revenue, not lost revenue.
- Revenue recognition occurs at credit consumption (publication), not at credit purchase.
- Detailed commercial rules, pricing, and credit mechanics are defined in COM-001.

---

## 17. Strategic Differentiators

What distinguishes Docsflip from alternative solutions.

### Output-Based Value Model

Revenue is tied to publication outputs, not platform access. This aligns Docsflip's commercial interests with customer success and removes the subscription barrier for occasional publishers. International competitors typically require recurring subscriptions regardless of publishing activity.

**Constitutional basis:** CON-001 PH-001, PP-001.

### Africa-First Design

The platform is designed for African payment methods, organisational structures, and publishing patterns from inception. International competitors treat African markets as secondary or design for developed-market assumptions.

**Constitutional basis:** CON-001 PH-006, PP-009.

### Transparent Commercial Philosophy

Costs are visible before commitment. Every transaction is recorded in an immutable ledger. There are no hidden fees, unexpected limitations, or silent credit consumption. This builds trust in markets where pricing opacity is common.

**Constitutional basis:** CON-001 PH-002, PP-003.

### Organisational Publishing Support

Workspaces, teams, roles, permissions, approval workflows, and consolidated billing are core platform capabilities — not enterprise-tier upsells. Organisations of any size can manage publishing as a team activity.

**Constitutional basis:** CON-001 PH-007, PP-007.

### Flexibility Across Publishing Frequencies

The platform serves publishers who publish once a year and those who publish daily without forcing either into an inappropriate commercial structure. Credit bundles scale with usage; subscriptions are optional.

**Constitutional basis:** CON-001 PP-005.

### Simplicity Over Complexity

The publishing flow is designed to be understood on first use. Feature accumulation is resisted — capabilities are added when they serve clear publishing needs, not to match competitor feature lists.

**Constitutional basis:** CON-001 PH-005, PP-001.

---

## 18. Foundational Business Decisions

1. **Publishing outcomes are the primary source of value.** Every business decision should be tested against whether it strengthens the publishing experience.

2. **Revenue should align with customer value creation.** Docsflip earns when customers publish — not when they maintain accounts, browse the platform, or occupy a subscription tier.

3. **Commercial mechanics must remain transparent.** Pricing, credit consumption, and publication costs must be visible before commitment. Trust is a business asset.

4. **Business strategy and commercial implementation are separate concerns.** BIZ-001 defines how the business creates and captures value. COM-001 defines the commercial engine that executes it.

5. **Africa is the design centre, not an expansion target.** Business assumptions, market strategies, and partnership decisions should be validated against African market realities.

6. **Organisational publishing is a core competency, not an upsell.** The platform's organisational capabilities should serve small NGOs and large government ministries with the same architectural foundation.

---

## 19. Architectural Integration Summary

BIZ-001 is the business strategy layer of the Docsflip documentation repository. It translates the Product Foundation (CON-001) and the Capability Framework (CAP-001 through CAP-005) into a structured business model. It depends on PA-001 for domain definitions and delegates commercial mechanics to COM-001.

### Dependency Map

```text
CON-001 (Product Foundation)
    │
    ▼
CAP-001 (Canonical Capability Model)
    │
    ▼
PA-001 (Product Architecture)
    │
    ▼
BIZ-001 (Business Model) ──► COM-001 (Commercial Rules)
    │
    ▼
USR-001 (Users & Stakeholders)
    │
    ▼
JNY-001 (User Journeys)
    │
    ▼
FEA-001 (Product Features)
    │
    ▼
REQ-001 (Product Requirements)
```

### Ownership Boundaries

| What BIZ-001 Owns                 | What BIZ-001 References                     |
| --------------------------------- | ------------------------------------------- |
| Business purpose and strategy     | CON-001 for product identity and philosophy |
| Value creation, delivery, capture | PA-001 for domain definitions               |
| Customer segment definition       | CAP-001/002 for capability traceability     |
| Market geography and channels     | COM-001 for commercial rules (does not own) |
| Business capabilities mapping     | USR-001 for user personas (does not own)    |
| Revenue stream definition         | ARC-001 for implementation (does not own)   |
| Strategic differentiation         |                                             |

### Upstream Dependencies

| Document | Dependency Type                                                  |
| -------- | ---------------------------------------------------------------- |
| CON-001  | Constitutional — business purpose derived from product identity  |
| CAP-001  | Constitutional — business capabilities trace to capability model |
| CAP-002  | Structural — capability decomposition for business mapping       |
| CAP-004  | Structural — publication as primary business asset               |
| PA-001   | Structural — domain vocabulary and bounded contexts              |

### Downstream Consumers

| Document | How BIZ-001 Is Used                                               |
| -------- | ----------------------------------------------------------------- |
| COM-001  | Revenue model and value capture logic inform commercial rules     |
| USR-001  | Customer segments inform user persona development                 |
| JNY-001  | Business model informs journey priorities and commercial journeys |
| FEA-001  | Business capabilities inform feature prioritisation               |
| REQ-001  | Business constraints inform requirements                          |

---

## 20. Refactoring State

**Loop 1 — Business Structure Alignment: COMPLETE.**
**Loop 2 — Business Content Expansion: COMPLETE.**
**Loop 3 — Architectural Integration: COMPLETE.**

BIZ-001 v0.4 is fully integrated into the Docsflip documentation repository with complete constitutional traceability (CON-001), capability traceability (CAP-001/002/004), domain traceability (PA-001), and downstream cross-references. All three implementation loops are complete.
