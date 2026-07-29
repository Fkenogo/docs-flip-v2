# DOCSFLIP-PA-001 — Product Architecture

**Document ID:** DOCSFLIP-PA-001  
**Title:** Product Architecture  
**Version:** 0.2 (Loop 1 — Structural Refactoring)  
**Status:** Active Draft  
**Maturity:** L1 — Skeleton (Structural Alignment Complete)  
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

The repository is developed in the following order:

```text
MP-001 → CON-001 → CAP-000 → { CAP-001 through CAP-005 } → PA-001 → BIZ-001 → COM-001 → USR-001 → JNY-001 → FEA-001 → REQ-001 → DAT-001 → ARC-001 → IMP-001
```

**Architectural Dependency Model**

```text
CON-001
    │
    ▼
CAP-001 (Canonical Capability Model)
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

PA-001 defines the following product architecture domains. Each top-level domain corresponds to exactly one Level 1 capability defined in CAP-001.

## Core Domains

### Identity

Individual accounts, authentication, profiles, credential lifecycle.

### Organisations

Organisation workspaces, teams, membership, workspace-level roles and permissions.

### Publications

The full lifecycle of digital publications, structured as three sub-domains:

- **Creation** — upload, validation, conversion, preview, publish.
- **Management** — hosting, metadata, ownership, availability, visibility, lifecycle, archival, restoration.
- **Distribution** — share links, embeds, QR codes, access policies.

The Publication is the primary business asset of Docsflip (CAP-004).

### Commercial

Credits, wallets, payments, entitlements, and publication output monetisation.

## Supporting Domains

### Reader Experience

Publication viewing, navigation, accessibility, search, and reader preferences.

### Analytics

Publication performance measurement, reader behaviour, publisher insights, and commercial reporting.

---

# 5. Deferred Concerns

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

# 6. Domain Relationships

Relationship model, lifecycle flow, and downstream traceability will be defined in WP-02R Loop 3 (Relationships and Traceability). The current relationship content from PA-001 v0.1 has been superseded by the structural refactoring.

---

# 7. Traceability

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

# 8. Foundational Decisions

1. **CAP-001 defines the canonical capability model.** PA-001 elaborates that model into architecture domains without inventing new Level 1 capabilities.

2. **PA-001 may not introduce a new Level 1 capability** without governance under CAP-005 and explicit Founder approval.

3. **The Publication remains the primary business asset of Docsflip** (CAP-004).

4. **Each top-level PA-001 domain corresponds to exactly one CAP-001 Level 1 capability.**

5. **PA-001 is independent of technology choices.** Implementation concerns are deferred to ARC-001.

6. **Downstream documents should align their structure to these domains.** Changes to core domains require Founder approval and CAP-005 governance.

---

# 9. Refactoring State

**Loop 1 — Structural Refactoring: COMPLETE.**

This document has been structurally refactored to align with the Capability Framework. The domain model has been reduced from 10 flat domains to 6 tiered domains matching CAP-001's Level 1 capabilities. Invented domains (Administration, Platform Services, Integrations) have been removed. Deferred concerns are assigned to ARC-001.

**Pending work:**

- **Loop 2 — Domain Content:** Detailed purpose, responsibilities, bounded contexts, asset ownership, and exclusions for each domain.
- **Loop 3 — Relationships and Traceability:** Lifecycle flow, dependency model, and complete downstream traceability.

Both loops require Founder authorisation before execution.
