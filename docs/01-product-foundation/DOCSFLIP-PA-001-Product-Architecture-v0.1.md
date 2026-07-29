# DOCSFLIP-PA-001 — Product Architecture

**Document ID:** DOCSFLIP-PA-001  
**Title:** Product Architecture  
**Version:** 0.3 (Loop 2 — Domain Content Expansion)  
**Status:** Active Draft  
**Maturity:** L2 — Expanded  
**Repository Path:** `docs/01-product-foundation/`  
**Authority:** Founder  
**Parent Documents:** DOCSFLIP-MP-001, DOCSFLIP-CON-001, DOCSFLIP-CAP-001  
**Governing Framework:** CAP-000 through CAP-005 (Authoritative)

---

# 1. Purpose

Product Architecture elaborates the canonical capability model defined by the Capability Framework (CAP-001) into enduring business domains, their responsibilities and relationships.

PA-001 does not invent capabilities. It translates the 6 Level 1 capabilities — Identity, Organisations, Publications, Reader Experience, Commercial, and Analytics — into an architecture vocabulary adopted by all downstream documents.

PA-001 is technology-independent. Implementation concerns identified during domain analysis are deferred to ARC-001 (Solution Architecture).

---

# 2. Position in the Documentation Hierarchy

**Execution Sequence**

```text
MP-001 → CON-001 → CAP-000 → { CAP-001 through CAP-005 } → PA-001 → BIZ-001 → COM-001 → USR-001 → JNY-001 → FEA-001 → REQ-001 → DAT-001 → ARC-001 → IMP-001
```

**Architectural Dependency Model**

```text
CON-001
    │
    ▼
CAP-001 (Canonical Capability Model — authoritative)
    │
    ▼
PA-001 (elaborates, does not invent)
 ├──────────────┬──────────────┐
 ▼              ▼              ▼
BIZ-001     COM-001      USR-001
                               │
                               ▼
                           JNY-001
                               ▼
                           FEA-001
                               ▼
                           REQ-001
                               ▼
                           DAT-001
                               ▼
                           ARC-001
                               ▼
                           IMP-001
```

---

# 3. Architectural Principles

- Domains represent business capabilities, not software modules.
- The architecture is technology-independent.
- Every downstream document adopts these domains.
- New capabilities should extend existing domains where practical.
- PA-001 may not introduce a new Level 1 capability without governance under CAP-005.

---

# 4. Core Product Domains

## 4.1 Identity (Core)

### Purpose

Identity owns individual user accounts, authentication, credential management, and personal profiles. It ensures that every person interacting with Docsflip has a secure, manageable, and privacy-respecting identity.

### Architectural Intent

Identity is the architectural entry point for all human actors. Every publisher, administrator, and contributor is recognised first through Identity before participating in any other domain. Identity enables trust without owning what users do once authenticated.

### Capability Owner

Identity — CAP-001 Level 1 capability.

### Business Assets

| Asset | Source  |
| ----- | ------- |
| User  | CAP-004 |

### Bounded Context

**Identity owns:** Individual user accounts, credentials, authentication sessions, personal profiles, account lifecycle states (active, suspended, recovery, closed), personal preferences.

**Identity does not own:** Organisational membership — that belongs to Organisations. Reader sessions — those belong to Reader Experience. What a user publishes — that belongs to Publications. Commercial entitlements — those belong to Commercial.

### Primary Responsibilities

- User registration and account creation.
- Authentication — verifying identity at login and throughout sessions.
- Credential management — password storage, reset, multi-factor support.
- Profile management — personal information, display preferences.
- Account lifecycle — activation, suspension, recovery, closure.
- Personal preference storage.
- Privacy and data protection controls for personal data.

### Key Sub-capabilities

Per CAP-002: Registration, Authentication, Profile Management, Account Lifecycle, Personal Preferences.

### Domain Principles

- One person, one identity — duplicate accounts should not be required for different contexts.
- Authentication enables trust; it does not grant authority — authority comes from Organisations or platform roles.
- Personal data belongs to the person — Identity governs its use.
- Identity is separable from organisational affiliation — an individual exists independently of any workspace.

### Domain Constraints

- Identity must not store organisational roles or permissions.
- Identity must not own commercial data (wallets, credits).
- Identity must not determine publishing capability — that is Commercial.
- Credential storage must follow security best practices (implementation deferred to ARC-001).

### Explicit Exclusions

- Organisation membership, team structures, roles, permissions → Organisations.
- Reader sessions → Reader Experience.
- Wallets, credits, payments → Commercial.
- Publication ownership → Publications.
- Authentication infrastructure, SSO protocol implementation → ARC-001.

### Dependencies

- Upstream: CON-001 (product identity), CAP-001 (capability definition).
- No domain-level upstream dependencies — Identity is self-standing.

### Downstream Consumers

| Document | How Identity is Used                                         |
| -------- | ------------------------------------------------------------ |
| USR-001  | User profiles and identity attributes for persona definition |
| JNY-001  | Registration and login journeys                              |
| FEA-001  | Authentication and profile features                          |
| REQ-001  | Identity-related functional requirements                     |
| DAT-001  | User entity and credential data model                        |
| ARC-001  | Authentication infrastructure implementation                 |

---

## 4.2 Organisations (Core)

### Purpose

Organisations owns collective workspaces, team structures, organisational membership, and workspace-level governance. It enables groups of users to collaborate, manage publishing workflows, and administer their organisational presence on Docsflip.

### Architectural Intent

Organisations is the bridge between individual identity and collective publishing. It provides the structural context within which teams operate, permissions are assigned, and organisational resources are managed. An organisation is a first-class entity — not a feature bolted onto individual accounts.

### Capability Owner

Organisations — CAP-001 Level 1 capability.

### Business Assets

| Asset        | Source  |
| ------------ | ------- |
| Organisation | CAP-004 |
| Workspace    | CAP-004 |
| Membership   | CAP-004 |

### Bounded Context

**Organisations owns:** Organisation entities, workspaces, membership records, workspace-level roles and permissions, team structures, member invitations, collaboration settings, organisation-level branding and configuration.

**Organisations does not own:** Individual user accounts — those belong to Identity. Commercial entitlements — those belong to Commercial. Publications — those belong to Publications (Organisations provides the organisational context in which publications exist). Platform-level administration — deferred to ARC-001.

### Primary Responsibilities

- Organisation creation and lifecycle management.
- Workspace management — creation, configuration, archival.
- Membership management — invitations, onboarding, offboarding, role assignment within the workspace.
- Team structures — groups, departments, project-based teams.
- Workspace-level permission assignment — who can publish, manage, administer within the workspace.
- Organisation branding and profile.
- Collaboration settings — shared drafts, team visibility.

### Key Sub-capabilities

Per CAP-002: Organisation Management, Workspace Management, Membership, Roles & Permissions, Invitations, Collaboration Settings.

### Domain Principles

- Organisations are first-class entities — not an upsell from individual accounts.
- Workspace governance is local — workspace roles do not grant platform-level authority.
- Membership is consensual — users accept invitations; organisations do not auto-enrol.
- An individual may belong to multiple organisations without identity duplication.

### Domain Constraints

- Organisations must not own individual user credentials or personal profiles.
- Workspace roles must not override platform-level access controls.
- Organisations must not own commercial entitlements — commercial capacity is allocated through Commercial, not Organisations.

### Explicit Exclusions

- Individual user accounts, authentication, personal profiles → Identity.
- Wallets, credits, payment processing → Commercial.
- Publication lifecycle, hosting → Publications.
- Platform administration, operator dashboards → ARC-001.

### Dependencies

- Upstream: Identity (for user authentication and membership linking).

### Downstream Consumers

| Document | How Organisations is Used                          |
| -------- | -------------------------------------------------- |
| BIZ-001  | Organisation customer segments, value delivery     |
| USR-001  | Organisation Administrator and Publisher personas  |
| JNY-001  | Organisation creation and team management journeys |
| FEA-001  | Workspace and team features                        |
| REQ-001  | Organisation-related functional requirements       |
| DAT-001  | Organisation, Workspace, Membership entities       |
| ARC-001  | Multi-tenancy implementation                       |

---

## 4.3 Publications (Core)

### Purpose

Publications owns the full lifecycle of digital publications — from document upload through conversion, publishing, hosting, management, distribution, and eventual archival or retirement. It is the central business capability of Docsflip.

### Architectural Intent

Publications is the architectural centre of Docsflip. The Publication is the primary business asset (CAP-004). Every other domain exists to create, govern, experience, commercialise, or measure publications. Publications is structured as three sub-domains recognising the distinct stages of the publication lifecycle: Creation, Management, and Distribution.

### Capability Owner

Publications — CAP-001 Level 1 capability.

### Business Assets

| Asset                | Source                                       |
| -------------------- | -------------------------------------------- |
| Publication          | CAP-004 (primary business asset of Docsflip) |
| Publication Metadata | CAP-004                                      |
| Publication Access   | CAP-004                                      |

### Bounded Context

**Publications owns:** The publication from upload to archival — PDF ingestion, validation, conversion/flipbook generation, preview, publish action, hosting, metadata, ownership tracking, availability/visibility control, lifecycle state management, sharing, embedding, QR codes, access policies.

**Publications does not own:** How publications are monetised — that belongs to Commercial. How publications are read — that belongs to Reader Experience. How publication performance is measured — that belongs to Analytics. Who owns the organisation publishing context — that belongs to Organisations.

---

### 4.3.1 Creation (Sub-domain)

#### Purpose

Creation transforms uploaded PDFs into validated, converted, previewable digital publications ready for publication.

#### Primary Responsibilities

- PDF upload and ingestion.
- File validation — format, size, page count, content integrity.
- Conversion — flipbook generation, page rendering, mobile optimisation.
- Preview — publisher-facing preview of the converted publication before commit.
- Publish — the atomic action that creates a live publication from a draft.

#### Key Sub-capabilities

Per CAP-002: Upload, Validation, Conversion, Preview, Publish.

#### Sub-domain Principles

- No publication is created without explicit publisher action.
- The publisher sees the publication before it goes live.
- Failed conversions must not silently consume credits — failure handling belongs to Commercial.

---

### 4.3.2 Management (Sub-domain)

#### Purpose

Management governs the ongoing life of a publication after creation — hosting, metadata, lifecycle states, ownership, availability, and retention.

#### Primary Responsibilities

- Hosting — publication availability on Docsflip infrastructure.
- Metadata — title, description, publication date, page count, cover image.
- Ownership — tracking which user/organisation owns the publication.
- Availability/Visibility — public, restricted, unlisted, private.
- Lifecycle states — active, renewal due, suspended, archived, deleted.
- Archival — moving publications to long-term retention.
- Restoration — recovering archived publications.
- Deletion — permanent removal after policy conditions.

#### Key Sub-capabilities

Per CAP-002: Hosting, Metadata, Ownership, Availability, Visibility, Lifecycle, Archive, Restore, Delete.

#### Sub-domain Principles

- The publisher owns the publication — Docsflip hosts it.
- Hosting has a defined duration and renewal model.
- Archival and deletion are deliberate, not automatic.
- Publication status is always visible to the owner.

---

### 4.3.3 Distribution (Sub-domain)

#### Purpose

Distribution enables publications to reach readers through shareable links, website embeds, QR codes, and access-controlled channels.

#### Primary Responsibilities

- Share link generation — permanent URLs for each publication.
- Embed code generation — iframe or script embeds for external websites.
- QR code generation — scannable codes linking to publications.
- Access policies — controlling who can access shared publications (public, restricted).

#### Key Sub-capabilities

Per CAP-002: Share Links, Embeds, QR Codes, Access Policies.

#### Sub-domain Principles

- Sharing does not transfer ownership — the publisher retains control.
- Access policies are enforced at the point of distribution, not at the reader.
- Embedded publications remain hosted by Docsflip — embeds are a distribution channel, not a hosting transfer.

---

### Domain Principles (Publications)

- The Publication is the primary business asset of Docsflip (CAP-004).
- Publications are created, managed, and distributed — not just uploaded and hosted.
- Every publication has a defined lifecycle with visible state.
- The publisher retains ownership — Docsflip provides the platform.

### Domain Constraints

- Publications must not own commercial monetisation logic.
- Publications must not define how publications are read (reader UI).
- Publications must not define how publication performance is measured.
- PDF content modification (editing) is explicitly excluded — Docsflip publishes documents, it does not edit them.

### Explicit Exclusions

- Document authoring, editing, design → out of product scope (CON-001 §7.2).
- Credit consumption, pricing, payment → Commercial.
- Publication viewer, reader navigation → Reader Experience.
- Publication metrics, reader behaviour → Analytics.
- File storage infrastructure, CDN → ARC-001.

### Dependencies

- Upstream: Identity (publisher identity), Organisations (organisational context).

### Downstream Consumers

| Document | How Publications is Used                                |
| -------- | ------------------------------------------------------- |
| COM-001  | Publication outputs as commercial triggers              |
| USR-001  | Publisher and contributor personas                      |
| JNY-001  | Upload, preview, publish, manage, share journeys        |
| FEA-001  | Publication creation, management, distribution features |
| REQ-001  | Publication-related functional requirements             |
| DAT-001  | Publication, metadata, access entities                  |
| ARC-001  | Conversion engine, hosting infrastructure, CDN          |

---

## 4.4 Commercial (Core)

### Purpose

Commercial owns the economic engine of Docsflip — credits, wallets, payments, entitlements, and publication output monetisation. It ensures that every commercial event is transparent, auditable, and tied to a publication outcome.

### Architectural Intent

Commercial translates the product philosophy of "pay for publishing outcomes" into a structured capability. It is the domain where value flows — credits are purchased, held, and consumed. Commercial does not set pricing strategy or payment provider rules — those belong to COM-001. PA-001 defines the commercial capability; COM-001 defines the commercial rules.

### Capability Owner

Commercial — CAP-001 Level 1 capability.

### Business Assets

| Asset   | Source  |
| ------- | ------- |
| Wallet  | CAP-004 |
| Credit  | CAP-004 |
| Payment | CAP-004 |

### Bounded Context

**Commercial owns:** Wallets, credit balances, credit purchase, credit consumption, payment initiation, entitlement management, publication output selection, cost preview, transaction history, country-aware commercial configuration.

**Commercial does not own:** Pricing strategy or specific price points — those belong to COM-001. Payment provider selection or gateway integration — that belongs to ARC-001. Publication lifecycle — that belongs to Publications. Business model or revenue strategy — that belongs to BIZ-001.

### Primary Responsibilities

- Wallet management — creation, balance tracking, lifetime record.
- Credit purchase — bundle selection, payment initiation, credit allocation.
- Credit consumption — deduction on publish, output selection, page extension.
- Cost preview — transparent display of costs before commitment (PH-002).
- Entitlement management — what a user/organisation can do based on credits held.
- Publication output pricing — base publication, page blocks, branding removal, embeds, self-hosted packages.
- Transaction history — immutable credit ledger.
- Country configuration — payment methods, currency, tax rules per country.
- Refund and adjustment handling (governed by COM-001 rules).

### Key Sub-capabilities

Per CAP-002: Wallet, Credits, Payments, Entitlements, Publication Outputs.

### Domain Principles

- Credits are consumed only for publication outputs (PH-001, PP-002).
- Cost is visible before commitment — no silent consumption (PH-002, PP-003).
- Purchased credits do not expire merely because time has passed (PH-003).
- Every transaction is traceable through an immutable ledger (PP-003).
- The user approves credit consumption before deduction.
- Country configuration enables market-aware commercial behaviour (PP-009).

### Domain Constraints

- Commercial must not own publication lifecycle states.
- Commercial must not determine what can be published — only what it costs.
- Commercial must not define pricing strategy — COM-001 defines rules.
- Payment provider integration is an ARC-001 concern.

### Explicit Exclusions

- Pricing strategy, credit values, bundle sizes → COM-001.
- Payment gateway integration, provider selection → ARC-001.
- Business strategy, revenue models → BIZ-001.
- Publication lifecycle, hosting → Publications.

### Dependencies

- Upstream: Publications (publishing events trigger commercial events), Identity (payer identity), Organisations (organisational commercial context).

### Downstream Consumers

| Document | How Commercial is Used                           |
| -------- | ------------------------------------------------ |
| COM-001  | Commercial rules, pricing, payment strategy      |
| BIZ-001  | Revenue models, value capture                    |
| USR-001  | Payer and administrator commercial personas      |
| JNY-001  | Credit purchase, cost approval, payment journeys |
| FEA-001  | Wallet, credit, payment features                 |
| REQ-001  | Commercial functional requirements               |
| DAT-001  | Wallet, Credit, Payment, Transaction entities    |
| ARC-001  | Payment gateway, ledger implementation           |

---

# 5. Supporting Domains

## 5.1 Reader Experience (Supporting)

### Purpose

Reader Experience owns how publications are consumed — reading, navigation, accessibility, search, and reader preferences. It ensures that every publication can be read by anyone, on any device, with or without assistive technology.

### Architectural Intent

Reader Experience is the consumer-facing domain. While Publications creates and distributes publications, Reader Experience defines what happens when a reader opens one. It is a first-class architecture concern because reading is a core product capability — not a side effect of publishing.

### Capability Owner

Reader Experience — CAP-001 Level 1 capability.

### Business Assets

| Asset          | Source  |
| -------------- | ------- |
| Reader Session | CAP-004 |

### Bounded Context

**Reader Experience owns:** Publication viewer, page navigation, zoom controls, search within publication, mobile-responsive viewing, accessibility features (screen reader support, keyboard navigation, contrast controls), reader preferences (font size, viewing mode), reading progress tracking.

**Reader Experience does not own:** Publication creation — that belongs to Publications. How publications are shared or embedded — that belongs to Publications → Distribution. Analytics collection — that belongs to Analytics (Reader Experience generates events; Analytics processes them).

### Primary Responsibilities

- Flipbook viewer rendering and performance.
- Page navigation — next/previous, thumbnails, table of contents.
- Zoom and pan controls.
- Search within publication.
- Mobile-responsive viewing — adaptive layout for phones, tablets, desktops.
- Accessibility — WCAG compliance, screen reader support, keyboard navigation, contrast.
- Reader preferences — font size, day/night mode, reading direction.
- Offline reading support (where applicable).
- Reader session management — anonymous reading, session continuity.

### Key Sub-capabilities

Per CAP-002: Reading, Navigation, Search, Accessibility, Reader Preferences.

### Domain Principles

- Every publication must be readable without requiring a Docsflip account — reading is open.
- The reader experience must work on low-bandwidth connections (PP-006).
- Accessibility is not optional — it is a product requirement (PP-006).
- The reader controls their reading experience — preferences are remembered.
- Reader Experience does not track readers for commercial purposes without consent.

### Domain Constraints

- Reader Experience must not collect personal data without consent.
- Reader Experience must not define what constitutes a publication — that is Publications.
- Reader Experience must not own analytics processing — it generates events, Analytics processes them.

### Explicit Exclusions

- Publication creation, conversion, hosting → Publications.
- Sharing, embedding, QR codes → Publications → Distribution.
- Analytics processing, reporting → Analytics.
- Notification delivery → ARC-001.
- Viewer rendering engine implementation → ARC-001.

### Dependencies

- Upstream: Publications (publication content and access control).

### Downstream Consumers

| Document | How Reader Experience is Used               |
| -------- | ------------------------------------------- |
| USR-001  | Publication Reader persona                  |
| JNY-001  | Reading and navigation journeys             |
| FEA-001  | Viewer, navigation, accessibility features  |
| REQ-001  | Reader-facing functional requirements       |
| DAT-001  | Reader Session entity                       |
| ARC-001  | Viewer engine, accessibility implementation |

---

## 5.2 Analytics (Supporting)

### Purpose

Analytics owns publication performance measurement, reader behaviour insights, publisher reporting, and commercial analytics. It transforms events from other domains into meaningful business intelligence.

### Architectural Intent

Analytics is a measurement domain, not a control domain. It observes what happens across Publications, Reader Experience, and Commercial, then provides insights to publishers and platform operators. Analytics does not define what should be measured — the source domains define what events they emit.

### Capability Owner

Analytics — CAP-001 Level 1 capability.

### Business Assets

| Asset            | Source  |
| ---------------- | ------- |
| Analytics Event  | CAP-004 |
| Analytics Report | CAP-004 |

### Bounded Context

**Analytics owns:** Event ingestion from Publications, Reader Experience, and Commercial; metric computation; report generation; publisher dashboards; geographic distribution; reader behaviour patterns.

**Analytics does not own:** The events it measures — Publications owns publication events, Reader Experience owns reader events, Commercial owns commercial events. Analytics does not define publishing rules or reader behaviour.

### Primary Responsibilities

- Publication performance metrics — views, unique readers, read-through rates, average reading time.
- Reader behaviour tracking — page engagement, navigation patterns, search queries.
- Publisher insights — aggregated performance data per publication and per publisher.
- Commercial reporting — credit consumption patterns, revenue analytics, payment trends.
- Geographic distribution data — where readers are located.
- Report generation — scheduled and on-demand reports for publishers.
- Event storage and retention.

### Key Sub-capabilities

Per CAP-002: Publication Metrics, Reader Behaviour, Publisher Insights, Commercial Reporting.

### Domain Principles

- Analytics measures outcomes — it does not control them.
- Publisher data belongs to the publisher — Analytics provides access, not ownership.
- Reader privacy is preserved — individual reader behaviour is anonymised.
- Reports should be understandable without technical expertise.

### Domain Constraints

- Analytics must not define what events are emitted — source domains define events.
- Analytics must not own publication, reader, or commercial data — it receives events.
- Analytics must not expose individual reader identities without consent.
- Event storage and processing infrastructure is deferred to ARC-001.

### Explicit Exclusions

- Publication event definition → Publications.
- Reader event definition → Reader Experience.
- Commercial event definition → Commercial.
- Event storage infrastructure, data pipeline → ARC-001.
- Business intelligence strategy → BIZ-001.

### Dependencies

- Upstream: Publications (publication events), Reader Experience (reader events), Commercial (commercial events).

### Downstream Consumers

| Document | How Analytics is Used                         |
| -------- | --------------------------------------------- |
| BIZ-001  | Market intelligence, performance metrics      |
| USR-001  | Publisher insights persona                    |
| JNY-001  | Review insights journey                       |
| FEA-001  | Analytics dashboard and reporting features    |
| REQ-001  | Analytics functional requirements             |
| DAT-001  | Analytics Event and Report entities           |
| ARC-001  | Event pipeline, data warehouse implementation |

---

# 6. Deferred Concerns

The following are not PA-001 business domains. Per CAP-001 §5, they belong in ARC-001 (Solution Architecture):

- APIs
- Integrations
- Cloud Storage
- Databases
- Infrastructure
- Notification Delivery Services
- Audit Infrastructure
- Platform Configuration
- Search-Engine Implementation
- Other Platform Services

No technical design is provided for these concerns in this document.

---

# 7. Domain Relationships

Relationship model, lifecycle flow, dependency diagrams, and complete downstream traceability will be defined in WP-02R Loop 3 (Relationships and Traceability).

---

# 8. Traceability

Every major artefact should reference one or more architecture domains:

- BIZ-001 → Value by domain
- COM-001 → Commercial domain
- USR-001 → User responsibilities by domain
- JNY-001 → Journeys across domains
- FEA-001 → Features grouped by domain
- REQ-001 → Requirements grouped by domain
- DAT-001 → Business entities by domain
- ARC-001 → Technical components implementing domains

---

# 9. Foundational Decisions

1. **CAP-001 defines the canonical capability model.** PA-001 elaborates that model into architecture domains without inventing new Level 1 capabilities.

2. **PA-001 may not introduce a new Level 1 capability** without governance under CAP-005 and explicit Founder approval.

3. **The Publication remains the primary business asset of Docsflip** (CAP-004).

4. **Each top-level PA-001 domain corresponds to exactly one CAP-001 Level 1 capability.**

5. **PA-001 is independent of technology choices.** Implementation concerns are deferred to ARC-001.

6. **Downstream documents should align their structure to these domains.** Changes to core domains require Founder approval and CAP-005 governance.

---

# 10. Refactoring State

**Loop 1 — Structural Refactoring: COMPLETE.**
**Loop 2 — Domain Content Expansion: COMPLETE.**

All 6 domains have defined purpose, architectural intent, capability owner, business assets, bounded context, primary responsibilities, key sub-capabilities, domain principles, domain constraints, explicit exclusions, dependencies, and downstream consumers.

**Pending work:**

- **Loop 3 — Relationships and Traceability:** Lifecycle flow, dependency model, and complete downstream traceability. Requires Founder authorisation.
