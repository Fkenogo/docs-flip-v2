# WP-02 Product Architecture Audit Report

**Work Package:** WP-02 — Expand PA-001 (Preparation)  
**Date:** 2026-07-29  
**Auditor:** Programme (structural analysis)  
**Document Audited:** DOCSFLIP-PA-001 v0.1 (L1 Skeleton)  
**Status:** Analytical — no expansion performed

---

## 1. Executive Assessment

The current PA-001 skeleton provides a reasonable starting point but requires substantial structural refinement before expansion. The 10-domain flat model captures most of the product's visible surface area but:

- **Lacks domain layering** — core, supporting, and cross-cutting capabilities are undifferentiated.
- **Has two boundary-critical overlaps** — Publishing vs Publication Management, Identity vs Organisation.
- **Contains one domain that may not belong** — Integrations is a technical/implementation concern, not a business capability.
- **Is missing domain homes** for document ingestion, preview, reader experience, country configuration, and notifications.
- **Has insufficient relationship modelling** — the current table captures adjacency but not lifecycle, authorisation, or flow.
- **Has weak constitutional traceability** — several domains have no clear anchor in CON-001.

**Overall readiness for expansion:** Requires Founder decisions on ~12 structural items before content expansion should begin.

---

## 2. Current-State Analysis

### 2.1 Purpose and Authority

PA-001 currently states its purpose as defining "the conceptual structure of Docsflip ... enduring business domains, their responsibilities and relationships without describing technical implementation."

This is appropriate. However:

- **Missing explicit statement of what PA-001 does NOT own.** It should disclaim ownership of business strategy (BIZ-001), commercial rules (COM-001), user profiles (USR-001), and technical design (ARC-001).
- **Relationship to CON-001 is implicit.** The hierarchy diagram shows dependency but the text does not explain how Product Architecture translates Product Identity into actionable structure.
- **Authority statement is absent.** PA-001 should declare itself as the authoritative domain vocabulary for all downstream documents.

### 2.2 Overlap Risk Assessment

| Concern         | Risk       | Detail                                                                                                                                                                   |
| --------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| CON-001 overlap | Low        | PA-001's domains are structural; CON-001 defines what the product is. The risk is in the Product Ecosystem section, which PA-001 should reference rather than replicate. |
| BIZ-001 overlap | Low        | PA-001 defines capability domains; BIZ-001 maps business value to them. No current overlap.                                                                              |
| COM-001 overlap | Medium     | "Commercial" domain (credits, wallets, payments) may drift into COM-001's territory if expanded with rules rather than capabilities.                                     |
| USR-001 overlap | Low-Medium | "Identity" domain includes "profiles" — PA-001 should define the capability boundary, not user personas.                                                                 |
| DAT-001 overlap | Low        | PA-001 is capability-level; DAT-001 is entity-level. Clear separation.                                                                                                   |
| ARC-001 overlap | Medium     | "Integrations" and "Platform Services" domains may drift into technical architecture. Needs guardrails.                                                                  |

---

## 3. Domain-by-Domain Assessment

### D1 — Identity

**Purpose:** Accounts, authentication, profiles and access.

**Assessment:**

- Core capability with strong constitutional support (PH-004 User Control, PP-004 User Control).
- "Profiles" may overlap with Organisation domain. Clarify: profiles belong to individuals; membership belongs to organisations.
- Missing explicit mention of authentication mechanisms — but this is appropriate at the capability level.
- **Recommendation:** Retain. Clarify boundary with Organisation. Add explicit responsibility for individual account lifecycle.

### D2 — Organisation

**Purpose:** Organisation workspaces, teams, governance and administration.

**Assessment:**

- Strong constitutional support (PH-007 Organisations Are First-Class Users, PP-007 Organisation-Ready).
- "Governance and administration" overlaps with Administration domain. Clarify: Organisation domain owns workspace-level governance (teams, roles, permissions within an organisation); Administration owns platform-level operational controls.
- **Recommendation:** Retain. Narrow "governance" to workspace governance. Separate platform administration clearly.

### D3 — Publishing

**Purpose:** Document upload, conversion, preview and publication.

**Assessment:**

- This is the central product domain. Strongest constitutional support (PH-001 Publishing Outcomes Define Value, PP-001 Publication-First).
- The current description bundles ingestion (upload), processing (conversion), preview, and publication into one domain. This is too broad.
- Publishing is a lifecycle, not a single capability. Consider whether "Document Ingestion," "Conversion" and "Publication" should be sub-domains or separate domains.
- **Recommendation:** Retain as a core domain but structure internally. Consider whether "preview" is a Publishing responsibility or a separate Reader Experience capability.

### D4 — Commercial

**Purpose:** Credits, wallets, pricing, payments and commercial policies.

**Assessment:**

- Strong constitutional support (PH-002 Transparency, PP-002 Pay for Value Delivered, PP-003 Transparency by Design).
- Overlaps with COM-001: PA-001 should define the Commercial capability domain; COM-001 should define the commercial rules operating within that domain.
- "Payments" as a capability may be better placed in a separate Payments capability under Commercial or as a cross-cutting concern.
- **Recommendation:** Retain. Clarify that PA-001 defines the capability; COM-001 defines the rules. Consider whether Payments warrants a sub-domain.

### D5 — Publication Management

**Purpose:** Hosting, lifecycle, renewal, archival and retirement.

**Assessment:**

- Enduring capability with constitutional support (CON-001 §7.1 Publication hosting, Publication management).
- The boundary with Publishing is the most critical architectural question in PA-001: does "Publishing" end when the publication is created, and "Publication Management" begin afterwards? Or is Publication Management a sub-capability of Publishing?
- **Recommendation:** Retain but resolve Publishing boundary. If Publishing and Publication Management are lifecycle stages of one domain, merge them. If they are distinct, define the handoff point precisely.

### D6 — Distribution

**Purpose:** Sharing, embeds, QR codes and access channels.

**Assessment:**

- Constitutional support from CON-001 §7.1 (Publication distribution).
- This domain is well-scoped and unlikely to overlap with others.
- "Access channels" may overlap with Reader Experience if that becomes a domain.
- **Recommendation:** Retain. Add explicit relationship to the publication reader.

### D7 — Analytics

**Purpose:** Usage, readership, engagement and reporting.

**Assessment:**

- Constitutional support from CON-001 §7.1 (Publication analytics).
- Well-scoped. The question is whether Analytics serves only publishers (publication performance) or also platform operators (platform health). Both are analytics but may be different sub-domains.
- **Recommendation:** Retain. Consider publisher analytics vs platform analytics separation.

### D8 — Administration

**Purpose:** Operational controls, support and platform administration.

**Assessment:**

- Weak constitutional support. CON-001 mentions "User and organisation management" in scope but does not establish platform administration as a product capability.
- "Support" is an operational concern, not necessarily a product domain.
- Overlaps with Organisation (workspace governance) and Platform Services (audit, configuration).
- **Recommendation:** Re-evaluate. Consider merging into Platform Services or splitting into distinct platform capabilities.

### D9 — Platform Services

**Purpose:** Notifications, configuration, audit and cross-cutting services.

**Assessment:**

- This domain is a technical grouping ("cross-cutting services") masquerading as a business capability.
- Notifications deliver user value (they are a product capability). Configuration and audit are technical/operational concerns.
- **Recommendation:** Split. Notifications should be elevated to a supporting domain or linked to Publishing/Distribution. Configuration and audit belong at the technical architecture level (ARC-001) or as non-domain concerns.

### D10 — Integrations

**Purpose:** Payment providers, storage, APIs and third-party services.

**Assessment:**

- This is a technical architecture concern, not a business capability. Users do not interact with "Integrations" — they interact with payment, storage, and third-party capabilities that may be implemented via integration.
- Payment providers belong under Commercial (as a capability), not as a separate domain.
- Storage is an infrastructure concern.
- APIs are a technical delivery mechanism.
- **Recommendation:** Remove as a domain. Redistribute: Payment integration → Commercial; Storage → Infrastructure concern (ARC-001); Third-party services → specific capability domains or ARC-001.

---

## 4. Missing-Domain Assessment

Capabilities from CON-001 and downstream documents that lack a clear architecture home:

| Capability                   | Current Home            | Assessment                                                                                             |
| ---------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------------ |
| Document ingestion           | Publishing (bundled)    | May warrant explicit recognition as a sub-domain of Publishing                                         |
| Conversion/processing        | Publishing (bundled)    | Publishing sub-domain or separate Processing capability                                                |
| Preview                      | Publishing (bundled)    | Could be Reader Experience or Publishing sub-domain                                                    |
| Publication lifecycle        | Publication Management  | Covered                                                                                                |
| Content ownership            | None                    | CON-001 Philosophy PH-004 (User Control) — needs a domain home (Identity or Publishing)                |
| Roles and permissions        | Organisation + Identity | Covered but boundary needs clarification                                                               |
| Credit/wallet management     | Commercial              | Covered                                                                                                |
| Payment processing           | Commercial (bundled)    | May warrant sub-domain or separate Payments capability                                                 |
| Reader experience            | None                    | **Critical gap.** CON-001 defines Publication Reader as a user category. Reading is a core capability. |
| Accessibility                | None                    | **Gap.** PP-006 Accessibility is a product principle with no architecture home                         |
| Country/region configuration | None                    | **Gap.** CON-001 Scope §7.1 (African payment support, configurable by country). Needs a domain home    |
| Notifications                | Platform Services       | Platform Services is too broad — notifications are a genuine product capability                        |
| Audit trail                  | Platform Services       | Technical concern, not a business capability                                                           |
| Customer/platform support    | Administration          | Operational concern                                                                                    |

---

## 5. Domain Boundary Analysis — Critical Pairs

### A. Publishing vs Publication Management

**Analysis:** The journey from upload to archival is a lifecycle. At what point does "Publishing" end and "Publication Management" begin?

**Option 1 — Single Publication Domain:** Merge Publishing and Publication Management into one "Publication" domain covering the full lifecycle. Simpler. Risks losing nuance.

**Option 2 — Lifecycle Separation:** Publishing = create + publish. Publication Management = host + manage + retire. Clean boundary but requires a clear handoff point.

**Option 3 — Sub-domains:** Publication as a core domain with Publishing and Publication Management as sub-domains.

**Recommendation:** Present all three options to Founder. Option 1 or 3 are preferred for simplicity.

### B. Identity vs Organisation

**Analysis:** Individual accounts and organisational membership are related but distinct.

**Identity owns:** Individual accounts, authentication, personal profiles, credential management.

**Organisation owns:** Workspaces, teams, organisational roles, member invitations, workspace governance.

**Overlap:** "Profiles" and "access" in Identity cross into Organisation when a profile operates within an organisational context.

**Recommendation:** Retain both domains. Define explicit boundary: Identity = individual; Organisation = collective.

### C. Commercial vs Payments

**Analysis:** Commercial is a broad domain. Payments could be:

- A sub-domain of Commercial
- A separate domain
- An implementation detail (ARC-001)

**Recommendation:** Keep Payments under Commercial as a sub-domain. PA-001 should acknowledge it as a capability without defining payment-provider mechanics.

### D. Administration vs Platform Services

**Analysis:** Both domains have weak constitutional support and technical leanings.

**Recommendation:** Present to Founder. Options:

- Merge into a single "Platform Operations" domain
- Dissolve both: operational capabilities → specific domains; technical concerns → ARC-001
- Retain Platform Services for genuine product-level cross-cutting services, remove Administration

### E. Integrations

**Analysis:** Not a business capability.

**Recommendation:** Remove from PA-001. Integration is an implementation strategy. Individual integration points belong to the domains they serve.

### F. Reader Experience

**Analysis:** CON-001 defines Publication Reader as a primary user category. Reading is a core product capability. No domain currently owns it.

**Recommendation:** Present to Founder. Options:

- Establish "Reader Experience" as a domain
- Assign reader capabilities to Distribution (which already owns sharing and access channels)
- Assign to a new "Consumption" or "Engagement" domain

---

## 6. Architecture-Level Options

Current model: **Flat list** of 10 domains.

Options for Founder consideration:

| Model                    | Description                         | Pros                                               | Cons                                                         |
| ------------------------ | ----------------------------------- | -------------------------------------------------- | ------------------------------------------------------------ |
| **Flat** (current)       | Single list of domains              | Simple, accessible                                 | Weak differentiation; cross-cutting concerns mixed with core |
| **Tiered**               | Core / Supporting / Cross-cutting   | Clarifies importance; guides downstream priority   | Requires Founder decision on tier assignment                 |
| **Tiered + Sub-domains** | Core domains with named sub-domains | Most precise; supports expansion without explosion | Heaviest structure; may over-engineer                        |

**Recommendation:** Tiered model (Core / Supporting / Cross-cutting). Core = Identity, Organisation, Publishing/Publication, Commercial. Supporting = Distribution, Analytics, Notifications, Reader Experience. Cross-cutting = configuration, audit (deferred to ARC-001 if technical).

---

## 7. Relationship-Model Options

Current model: **Adjacency table** — lists "primary relationships" per domain.

Options:

| Model                   | Description                                       |
| ----------------------- | ------------------------------------------------- |
| **Adjacency** (current) | Bi-directional relationship pairs                 |
| **Dependency**          | Upstream/downstream dependency graph              |
| **Lifecycle**           | Domain interactions by publishing lifecycle stage |
| **Authorisation**       | Which domains control actions in other domains    |

**Recommendation:** Combine Adjacency + Lifecycle. The adjacency table captures structural relationships; a lifecycle model captures the publishing flow through domains. Authorisation relationships should be noted within each domain's boundary definition.

---

## 8. Constitutional Traceability

Mapping PA-001 domains to CON-001:

| Domain                 | PH Support             | PP Support             | Scope Support                                    | Strength                         |
| ---------------------- | ---------------------- | ---------------------- | ------------------------------------------------ | -------------------------------- |
| Identity               | PH-004                 | PP-004                 | User management                                  | Strong                           |
| Organisation           | PH-007                 | PP-007                 | User management                                  | Strong                           |
| Publishing             | PH-001, PH-003, PH-005 | PP-001, PP-005, PP-008 | Document conversion, Publication management      | Very Strong                      |
| Commercial             | PH-002                 | PP-002, PP-003         | Commercial transparency, African payment support | Strong                           |
| Publication Management | PH-001                 | PP-001, PP-008         | Publication hosting, Publication management      | Strong                           |
| Distribution           | —                      | PP-006                 | Publication distribution                         | Moderate                         |
| Analytics              | —                      | —                      | Publication analytics                            | Weak — needs PP anchoring        |
| Administration         | —                      | —                      | —                                                | Weak — no direct CON-001 support |
| Platform Services      | —                      | —                      | —                                                | Weak — no direct CON-001 support |
| Integrations           | —                      | —                      | —                                                | Weak — no direct CON-001 support |

**Domains with weak or no constitutional support:** Analytics, Administration, Platform Services, Integrations. These require either stronger CON-001 traceability or reclassification as non-domain concerns.

---

## 9. Legacy and Downstream Discovery

### Legacy Concept Document findings:

- The concept document extensively discusses credits, pricing, payment methods, and hosting — these align with Commercial and Publication Management domains.
- No mention of "Integrations" or "Platform Services" as user-facing concepts.
- Reader experience is described implicitly (viewer, mobile-responsive, accessibility) but not named as a capability.
- Country configuration for payments is discussed — supports the need for a configuration capability.

### Downstream skeleton findings:

- JNY-001's 10 core journeys map cleanly to current domains: J1→Distribution, J2-J3→Identity/Organisation, J4-J5→Publishing, J6→Commercial, J7→Publishing, J8→Distribution, J9→Publication Management, J10→Analytics.
- FEA-001 and REQ-001 are skeletons with no domain references yet — they will depend on PA-001 for structure.
- BIZ-001 references "Key Capabilities" that partially match domains but uses different terminology ("Digital publishing" vs "Publishing," "Customer support" vs "Administration").

---

## 10. Risks and Assumptions

| Risk                                                                                             | Severity | Mitigation                                               |
| ------------------------------------------------------------------------------------------------ | -------- | -------------------------------------------------------- |
| Publishing/Publication Management boundary misalignment creates downstream confusion             | High     | Resolve before expansion; Founder decision required      |
| Integrations domain removal disrupts COM-001 traceability (COM-001 references payment providers) | Medium   | Payment capability stays under Commercial; no disruption |
| Weak constitutional support for Administration, Platform Services, Analytics                     | Medium   | Either strengthen CON-001 traceability or reclassify     |
| Reader Experience gap leaves a core user need unowned                                            | High     | Address in Founder Decision Agenda                       |
| Tiered model over-engineering creates unnecessary complexity                                     | Low      | Start simple; tiers can be added incrementally           |

---

## 11. Recommended Direction

1. **Adopt a tiered domain model** (Core / Supporting / Cross-cutting) with sub-domain structure where needed.
2. **Resolve Publishing vs Publication Management** before expansion — either merge or define precise boundary.
3. **Remove Integrations** as a domain — redistribute to specific capability domains.
4. **Split Platform Services** — elevate Notifications to a supporting domain; defer configuration/audit to ARC-001.
5. **Establish Reader Experience** as a new domain or sub-domain.
6. **Add Country Configuration** capability under a suitable domain (Commercial or a new Configuration domain).
7. **Add Accessibility** as a cross-cutting principle, not necessarily a domain.
8. **Re-evaluate Administration** — merge, split or remove.

---

## 12. Items Safe for Drafting (No Founder Decision Required)

- Domain purpose statements for Identity, Organisation, Publishing, Commercial, Distribution (once boundary issues are resolved).
- Constitutional traceability mapping for each domain.
- Relationship model (adjacency table) for agreed domains.
- Downstream traceability rules.

## 13. Items Requiring Founder Decision

Presented in the WP-02 Founder Decision Agenda.
