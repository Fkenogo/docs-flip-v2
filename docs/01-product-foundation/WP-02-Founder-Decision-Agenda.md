# WP-02 Founder Decision Agenda — Product Architecture

**Work Package:** WP-02 — Expand PA-001 (Preparation)  
**Date:** 2026-07-29  
**Status:** For Founder review — no decisions recorded  
**Authority Required:** Founder

---

## Agenda Summary

12 decisions are presented for Founder determination before PA-001 expansion can begin. Each decision includes the question, options, auditor recommendation, and implications.

Decisions are grouped: 4 structural (affecting the domain model), 4 boundary (resolving overlaps), and 4 new-domain (establishing or declining new architecture entities).

---

## SECTION A — Structural Decisions

### DA-001 — Architecture Model

**Question:** Should PA-001 use a flat domain list, a tiered model (Core / Supporting / Cross-cutting), or a tiered model with sub-domains?

**Context:** The current skeleton uses a flat list of 10 domains. Flat models do not distinguish between foundational capabilities and supporting services. A tiered model guides downstream priority and clarifies which domains are architecturally significant.

**Options:**

| Option                       | Description                                     | Implications                                                                                                |
| ---------------------------- | ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **A — Flat**                 | Retain current single-level domain list         | Simplest. No structural change. Weak differentiation between core and peripheral capabilities.              |
| **B — Tiered**               | Core / Supporting / Cross-cutting tiers         | Clarifies importance. Guides downstream document priority. Requires Founder assignment of domains to tiers. |
| **C — Tiered + Sub-domains** | Tiers plus named sub-domains under core domains | Most precise. Supports expansion without domain explosion. Heaviest structure.                              |

**Auditor Recommendation:** Option B — Tiered.

---

### DA-002 — Publishing vs Publication Management

**Question:** Should Publishing and Publication Management remain separate domains, or be merged into a single Publication domain?

**Context:** Publishing currently covers upload, conversion, preview and publication. Publication Management covers hosting, lifecycle, renewal, archival and retirement. These represent two stages of a single publication lifecycle. The boundary between them is the most critical architectural decision in PA-001.

**Options:**

| Option                                      | Description                                                                      | Implications                                                                                   |
| ------------------------------------------- | -------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **A — Merge into one "Publication" domain** | Single domain covering full lifecycle                                            | Simplest. Eliminates boundary ambiguity. May be too broad for one domain.                      |
| **B — Retain both with defined handoff**    | Publishing = create + publish; Publication Management = host + manage + retire   | Clean conceptual separation. Requires precise handoff definition.                              |
| **C — Publication domain with sub-domains** | Publication as core domain; Publishing and Publication Management as sub-domains | Best of both. Retains conceptual clarity of two concerns while acknowledging shared lifecycle. |

**Auditor Recommendation:** Option C — Publication domain with Publishing and Publication Management as sub-domains.

---

### DA-003 — Administration Domain Fate

**Question:** Should Administration be retained, merged into another domain, or removed and its capabilities distributed?

**Context:** Administration has weak constitutional support. Its current responsibilities (operational controls, support) overlap with Organisation (workspace governance) and Platform Services (audit, configuration). "Support" is an operational concern, not necessarily a product capability.

**Options:**

| Option                               | Description                                                                                                | Implications                                                                     |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **A — Retain**                       | Keep Administration as a platform operations domain                                                        | Maintains current structure. Requires strengthening constitutional traceability. |
| **B — Remove and distribute**        | Move capabilities to Organisation (workspace admin), Platform Services or a new domain (operational admin) | Cleaner architecture. No single "admin" catch-all.                               |
| **C — Merge into Platform Services** | Combine Administration and Platform Services                                                               | Consolidates two weak domains. Still a technical grouping concern.               |

**Auditor Recommendation:** Option B — Remove and distribute capabilities.

---

### DA-004 — Integrations Domain Removal

**Question:** Should Integrations be removed as a product architecture domain?

**Context:** Integrations is a technical implementation strategy, not a business capability. Users interact with payment, storage, and third-party services — not with "integrations." Payment providers logically belong under Commercial. Storage is infrastructure. APIs are a delivery mechanism.

**Options:**

| Option         | Description                                                       | Implications                                                                                           |
| -------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **A — Remove** | Delete Integrations as a domain. Redistribute to specific domains | Cleaner architecture. Payment capability moves to Commercial. Technical integrations defer to ARC-001. |
| **B — Retain** | Keep Integrations as a domain                                     | Preserves current structure. Risks conflating capability with implementation.                          |

**Auditor Recommendation:** Option A — Remove.

---

## SECTION B — Boundary Decisions

### DA-005 — Platform Services Fate

**Question:** Should Platform Services be split, retained, or removed?

**Context:** Platform Services currently bundles Notifications (a genuine product capability) with configuration, audit, and cross-cutting services (technical concerns). This makes it a mixed-domain.

**Options:**

| Option                    | Description                                                                                      | Implications                                                                                                |
| ------------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------- |
| **A — Split**             | Notifications → new supporting domain; Configuration → Commercial or new domain; Audit → ARC-001 | Cleanest separation. Removes the "Platform Services" name. Requires establishing Notifications as a domain. |
| **B — Retain but narrow** | Keep Platform Services for notifications only; move other concerns                               | Simpler. Retains a domain name that is already used.                                                        |
| **C — Remove entirely**   | All capabilities redistributed; no Platform Services domain                                      | Cleanest. Requires all current Platform Services items to find new homes.                                   |

**Auditor Recommendation:** Option A — Split.

---

### DA-006 — Identity vs Organisation Boundary

**Question:** What is the precise boundary between the Identity and Organisation domains?

**Context:** Identity currently includes "profiles and access" which blurs into Organisation's "workspaces, teams, governance." The boundary should be: Identity = individual accounts; Organisation = collective workspaces.

**Options:**

| Option                           | Description                                                                    | Implications                                                                          |
| -------------------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------- |
| **A — Individual vs Collective** | Identity owns individual accounts; Organisation owns workspaces and membership | Clear boundary. Supported by CON-001 user categories.                                 |
| **B — Merge**                    | Combine Identity and Organisation into one "Users & Access" domain             | Simpler. Loses conceptual distinction between individual and organisational identity. |
| **C — Identity superset**        | Identity is the parent; Organisation is a sub-domain                           | Clean hierarchy. May over-elevate Identity.                                           |

**Auditor Recommendation:** Option A — Individual vs Collective.

---

### DA-007 — Commercial Boundary with COM-001

**Question:** How should PA-001's Commercial domain relate to COM-001's Commercial Architecture?

**Context:** PA-001 defines capabilities (what the platform can do). COM-001 defines commercial rules (how value is measured, charged, purchased). The current skeleton risks drifting into rule definition.

**Resolution proposed (not an option — for confirmation):** PA-001 defines the Commercial capability domain (credits, wallets, payment capability). COM-001 defines the rules operating within that domain (credit values, pricing, ledgers, payment strategy). This is consistent with the established document separation.

**Founder Confirmation Required:** Confirm this capability-vs-rules boundary.

---

### DA-008 — Analytics Scope

**Question:** Should Analytics be split into Publisher Analytics and Platform Analytics?

**Context:** Publishers need publication performance data. Platform operators need platform health data. These serve different users and have different data sources. The current skeleton does not distinguish them.

**Options:**

| Option                | Description                                               | Implications                                                                      |
| --------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **A — Split**         | Publisher Analytics and Platform Analytics as sub-domains | Clear separation of concerns. Platform Analytics may be deferred to later phases. |
| **B — Single domain** | Keep Analytics as one domain with both scopes             | Simpler. Risk of conflating publisher and operator needs.                         |

**Auditor Recommendation:** Option A — Split with sub-domains.

---

## SECTION C — New-Domain Decisions

### DA-009 — Reader Experience Domain

**Question:** Should a Reader Experience domain be established? If so, where?

**Context:** CON-001 defines Publication Reader as a primary user category. PP-006 requires accessibility. The publication viewer, navigation, and reading experience have no architecture home.

**Options:**

| Option                             | Description                                                              | Implications                                                                         |
| ---------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| **A — New supporting domain**      | Establish Reader Experience as a separate supporting domain              | Full recognition of reader as first-class architecture concern. Aligns with CON-001. |
| **B — Sub-domain of Distribution** | Place reader experience under Distribution (which owns access channels)  | Logical adjacency but conflates distribution (sharing) with consumption (reading).   |
| **C — Sub-domain of Publishing**   | Place reader experience under Publishing (which creates the publication) | Logical but Publishing is publisher-facing; reader is consumer-facing.               |
| **D — No separate domain**         | Keep reader concerns in Distribution or Publishing                       | Simplest. Weakens architecture traceability for reader-focused capabilities.         |

**Auditor Recommendation:** Option A — New supporting domain.

---

### DA-010 — Notifications Domain

**Question:** Should Notifications be established as a separate supporting domain?

**Context:** Notifications are currently bundled in Platform Services. They are a genuine cross-domain product capability — publishing events, commercial alerts, hosting reminders all generate notifications. PH-002 Transparency and PP-003 Transparency by Design provide constitutional support.

**Options:**

| Option                         | Description                                            | Implications                                                                       |
| ------------------------------ | ------------------------------------------------------ | ---------------------------------------------------------------------------------- |
| **A — New supporting domain**  | Establish Notifications as a separate domain           | Clean architecture. Clear ownership of notification rules, templates, preferences. |
| **B — Keep within Publishing** | Fold notifications into the domains that generate them | No central notification management. Each domain manages its own notifications.     |
| **C — Defer to ARC-001**       | Treat notifications as a technical concern             | Notifications are a user-facing product capability — not appropriate for ARC-001.  |

**Auditor Recommendation:** Option A — New supporting domain.

---

### DA-011 — Country Configuration Home

**Question:** Where should country-specific configuration reside?

**Context:** CON-001 Scope §7.1 requires "African payment support — supporting payment methods relevant to African markets, configurable by country." PP-009 Market-Aware reinforces this. No domain currently owns country-aware configuration.

**Options:**

| Option                             | Description                                                                         | Implications                                                                                  |
| ---------------------------------- | ----------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **A — Sub-domain of Commercial**   | Country configuration under Commercial (payment methods, currency, tax per country) | Tight coupling with commercial capability. Logical: most country configuration is commercial. |
| **B — Separate supporting domain** | Standalone "Country Configuration" or "Localisation" domain                         | More flexible if non-commercial country configuration emerges. Adds a domain.                 |
| **C — Cross-cutting concern**      | Not a domain — a configuration capability used by all domains                       | Lighter weight. Risks scattering country logic across multiple domains.                       |

**Auditor Recommendation:** Option A — Sub-domain of Commercial.

---

### DA-012 — Accessibility as Architecture Principle

**Question:** Should Accessibility be established as a domain, or treated as a cross-cutting architecture principle?

**Context:** PP-006 Accessibility requires digital publications to be "accessible across devices, connection qualities and user capabilities." The Reader Experience domain can own accessibility implementation, but accessibility may be broader than any single domain.

**Options:**

| Option                                  | Description                                                           | Implications                                                                                            |
| --------------------------------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **A — Cross-cutting principle**         | Accessibility is a principle applied across all reader-facing domains | No separate domain. Principle enforced during expansion of Reader Experience, Distribution, Publishing. |
| **B — Sub-domain of Reader Experience** | Accessibility owned by Reader Experience                              | Clear ownership but may miss accessibility beyond the reader (e.g., publisher-facing accessibility).    |
| **C — Separate domain**                 | Dedicated Accessibility domain                                        | Over-engineering for a cross-cutting concern.                                                           |

**Auditor Recommendation:** Option A — Cross-cutting principle. Do not create a separate Accessibility domain.

---

## Decision Summary

| Ref    | Decision                             | Options                                                     | Auditor Recommendation       | Priority                           |
| ------ | ------------------------------------ | ----------------------------------------------------------- | ---------------------------- | ---------------------------------- |
| DA-001 | Architecture model                   | Flat / Tiered / Tiered+Sub                                  | Tiered                       | Critical — shapes entire document  |
| DA-002 | Publishing vs Publication Management | Merge / Separate / Sub-domains                              | Publication with sub-domains | Critical — most impactful boundary |
| DA-003 | Administration fate                  | Retain / Remove / Merge                                     | Remove and distribute        | High                               |
| DA-004 | Integrations removal                 | Remove / Retain                                             | Remove                       | High                               |
| DA-005 | Platform Services fate               | Split / Narrow / Remove                                     | Split                        | High                               |
| DA-006 | Identity/Organisation boundary       | Individual/Collective / Merge / Superset                    | Individual vs Collective     | Medium                             |
| DA-007 | Commercial/COM-001 boundary          | Confirm capability vs rules                                 | Confirm                      | Medium                             |
| DA-008 | Analytics scope                      | Split / Single                                              | Split with sub-domains       | Medium                             |
| DA-009 | Reader Experience domain             | New domain / Sub of Distribution / Sub of Publishing / None | New supporting domain        | High                               |
| DA-010 | Notifications domain                 | New domain / Keep in domains / Defer to ARC                 | New supporting domain        | Medium                             |
| DA-011 | Country Configuration home           | Sub of Commercial / Separate / Cross-cutting                | Sub-domain of Commercial     | Medium                             |
| DA-012 | Accessibility treatment              | Principle / Sub-domain / Domain                             | Cross-cutting principle      | Low                                |

**12 decisions requiring Founder determination.**
