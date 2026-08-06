# COM-WP04-007 — Commercial Architecture Expansion Blueprint

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised  
**Target Document:** DOCSFLIP-COM-001 v0.1 → v0.4 (L1 → L2) _upon implementation_

---

## 1. Purpose

This blueprint defines the proposed target structure for COM-001 expansion. It regroups the existing 8 skeleton components into a coherent 9-part commercial architecture framework, preserving all existing content and adding the missing commercial surface identified in COM-WP04-001/004.

The structure follows the grouping requested in the task brief:

- Commercial Foundation;
- Credit and Wallet Model;
- Publication Output Commercial Model;
- Pricing and Entitlements;
- Payments and Market Support;
- Organisation and Enterprise Commercial Model;
- Hosting, Renewal and Account Lifecycle;
- Governance, Exceptions and Traceability.

---

## 2. Target Structure

### Part 1 — Commercial Foundation

| Proposed Section                      | Purpose                                                | Preserves   | Adds (Required)                                                                           |
| ------------------------------------- | ------------------------------------------------------ | ----------- | ----------------------------------------------------------------------------------------- |
| §1 Purpose                            | Defines COM-001's role                                 | Skeleton §1 | Explicit architectural boundary (peer of BIZ-001/USR-001; content dependency on BIZ-001)  |
| §2 Document Responsibility            | "COM-001 owns / does not own"                          | —           | Ownership boundary statement (mirrors BIZ-001 §2 pattern)                                 |
| §3 Commercial Philosophy              | 5 principles                                           | Skeleton §2 | **Explicit CON-001 PH/PP citations** (PH-001/002/003/005/006, PP-001/002/003/005/007/009) |
| §4 Commercial Model Overview          | Pay-as-you-publish                                     | Skeleton §3 | Revenue-recognition boundary (BIZ-001 §16) as constraint                                  |
| §5 Settled Constitutional Constraints | Non-expiry, optional subscriptions, output-based value | —           | Codify the 9 settled constraints (COM-WP04-006 §5)                                        |

### Part 2 — Credit and Wallet Model

| Proposed Section  | Purpose                                   | Preserves                 | Adds (Required)                                                                                                                                                                    |
| ----------------- | ----------------------------------------- | ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| §6 Credit Economy | Credit definition, nature, representation | Skeleton §5               | Credit acquisition; consumption rules; non-expiry implementation; promotional credits (subject to Founder decision); credit denominations; minimum bundle (subject to FD-02)       |
| §7 Credit Ledger  | Immutable history                         | Skeleton §7 (ledger part) | Ledger immutability rules; auditability; transaction categories                                                                                                                    |
| §8 Wallet Model   | Wallet behaviour                          | Skeleton §7 (wallet part) | Wallet ownership model; wallet lifecycle; cost preview before deduction (PH-002); user approval before consumption (PP-003); wallet closure / inactive handling (subject to FD-01) |

### Part 3 — Publication Output Commercial Model

| Proposed Section                              | Purpose                               | Preserves          | Adds (Required)                                                                                            |
| --------------------------------------------- | ------------------------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------- |
| §9 Publication Output Definition              | What constitutes a publication output | Skeleton §6 (core) | Precise commercial definition grounded in CON-001 PH-001; output-event catalogue                           |
| §10 Base Publication Model                    | Base cost and page allowance          | Skeleton §6        | Base page allowance (subject to FD-04); base vs add-on separation (subject to FD-03)                       |
| §11 Additional Pages                          | Page extension charging               | —                  | Additional-page charging mechanics (subject to FD-05)                                                      |
| §12 Output Add-Ons                            | Optional outputs                      | —                  | Branding removal, embeds, offline, self-hosted, advanced analytics (BIZ-001 §16); add-on pricing mechanics |
| §13 Republishing and Post-Publication Changes | Update consumption                    | —                  | Republishing consumption rules (subject to FD-08)                                                          |

### Part 4 — Pricing and Entitlements

| Proposed Section         | Purpose            | Preserves   | Adds (Required)                                                                                                                 |
| ------------------------ | ------------------ | ----------- | ------------------------------------------------------------------------------------------------------------------------------- |
| §14 Pricing Architecture | Pricing principles | Skeleton §8 | Pricing architecture vs strategy boundary (PA-001 §4.4); base/add-on price structure; price-point governance (subject to FD-12) |
| §15 Entitlements         | What credits allow | —           | **Entitlements model** (CAP-001 §2; PA-001 §4.4): publish, renew, add-ons, organisation allocations                             |

### Part 5 — Payments and Market Support

| Proposed Section                     | Purpose                | Preserves   | Adds (Required)                                                                                                                                                      |
| ------------------------------------ | ---------------------- | ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| §16 Payment Strategy                 | Payment methods        | Skeleton §9 | Payment method types (mobile money, card, invoicing — BIZ-001 §11); payment initiation; provider-abstraction boundary (ARC-001 implements, COM-001 defines strategy) |
| §17 Country Commercial Configuration | African market support | —           | Country configuration framework; currency rules; tax rules (PA-001 §4.4; BIZ-001 §11); East Africa launch configuration                                              |

### Part 6 — Organisation and Enterprise Commercial Model

| Proposed Section                  | Purpose                 | Preserves    | Adds (Required)                                                                                                                                    |
| --------------------------------- | ----------------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| §18 Organisation Commercial Model | Organisation mechanics  | Skeleton §10 | Organisation credit allocation; admin commercial controls (CON-001 §8); approval workflows; subscription/allocation coexistence (subject to FD-10) |
| §19 Enterprise and Procurement    | Enterprise arrangements | —            | Enterprise overlay model (subject to FD-11); invoicing; purchase orders; volume commitments; negotiated contracts (BIZ-001 §6, §8)                 |

### Part 7 — Hosting, Renewal and Account Lifecycle

| Proposed Section      | Purpose                       | Preserves    | Adds (Required)                                                                                                                         |
| --------------------- | ----------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| §20 Hosting Lifecycle | Activation, duration, renewal | Skeleton §11 | Included hosting duration (subject to FD-06); renewal mechanics (subject to FD-07); archival/retirement commercial terms (CON-001 §7.1) |
| §21 Account Lifecycle | Commercial account states     | —            | Dormant/inactive accounts with credits (subject to FD-01); account closure commercial handling                                          |

### Part 8 — Governance, Exceptions and Traceability

| Proposed Section                     | Purpose                        | Preserves                    | Adds (Required)                                                                                                         |
| ------------------------------------ | ------------------------------ | ---------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| §22 Commercial Governance Principles | Transparency etc.              | Skeleton §12                 | Expand into full governance section                                                                                     |
| §23 Commercial Exceptions            | Non-standard commercial events | —                            | Exception governance framework (who approves, how recorded)                                                             |
| §24 Traceability                     | Evidence mapping               | Skeleton §13 (relationships) | **Full traceability tables**: CAP-001/002/004, PA-001 §4.4, BIZ-001 content inputs, CON-001 PH/PP, downstream consumers |

### Part 9 — Foundational Decisions

| Proposed Section         | Purpose                             | Preserves    | Adds (Required)                                                                                          |
| ------------------------ | ----------------------------------- | ------------ | -------------------------------------------------------------------------------------------------------- |
| §25 Commercial Decisions | Constitutional commercial decisions | Skeleton §14 | Expand to full Foundational Decisions section codifying settled constraints + Founder-approved decisions |

---

## 3. Structure Rationale

| Design Choice                        | Reason                                                                                                                                                             |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 9 parts / 25 sections                | Proportionate to the commercial surface defined by PA-001 §4.4 and BIZ-001 §6/§16; aligns with established pattern of PA-001 (6 domains) and BIZ-001 (20 sections) |
| Commercial Foundation first          | Mirrors BIZ-001's Part 1 Value Model pattern — establish boundaries and constitutional basis before mechanics                                                      |
| Credit + Wallet as Part 2            | Accounts for the commercial engine's core                                                                                                                          |
| Entitlements placed near Pricing     | Entitlements bridge pricing (what costs) to capability (what credits allow) — cohesive                                                                             |
| Payments + Market Support together   | Payment methods, currency, tax, country config are one commercial surface (PA-001 §4.4 country-aware configuration)                                                |
| Organisation + Enterprise together   | Organisation (standard) and Enterprise (negotiated overlay) are one commercial family                                                                              |
| Hosting + Account Lifecycle together | Hosting states and account states share lifecycle logic                                                                                                            |
| Governance + Traceability last       | Mirror BIZ-001 §19-20 pattern (integration at the end)                                                                                                             |
| All 8 skeleton components preserved  | No content loss; each existing section maps to a new section (see migration in COM-WP04-008)                                                                       |

---

## 4. Source Component Preservation Map

| Current Skeleton §                   | Preserved In            |
| ------------------------------------ | ----------------------- |
| §1 Purpose                           | §1                      |
| §2 Commercial Philosophy             | §3                      |
| §3 Commercial Model Overview         | §4                      |
| §4 Commercial Components             | §2 (structure overview) |
| §5 Credit Economy                    | §6                      |
| §6 Publication Output Model          | §9-10                   |
| §7 Wallet & Ledger                   | §7-8                    |
| §8 Pricing Architecture              | §14                     |
| §9 Payment Strategy                  | §16                     |
| §10 Organisation Commercial Model    | §18                     |
| §11 Publication Hosting Lifecycle    | §20                     |
| §12 Commercial Governance Principles | §22                     |
| §13 Relationships                    | §24                     |
| §14 Commercial Decisions             | §25                     |

---

## 5. Content Volume Estimate

| Part                            | Sections | Source Lines (approx) | Target Content Units (approx) |
| ------------------------------- | -------- | --------------------- | ----------------------------- |
| 1 — Commercial Foundation       | 5        | 40                    | 15                            |
| 2 — Credit & Wallet             | 3        | 30                    | 20                            |
| 3 — Publication Output          | 5        | 20                    | 25                            |
| 4 — Pricing & Entitlements      | 2        | 15                    | 12                            |
| 5 — Payments & Market           | 2        | 15                    | 12                            |
| 6 — Organisation & Enterprise   | 2        | 10                    | 12                            |
| 7 — Hosting & Account Lifecycle | 2        | 10                    | 12                            |
| 8 — Governance & Traceability   | 3        | 15                    | 20                            |
| 9 — Foundational Decisions      | 1        | 5                     | 10                            |
| **Total**                       | **25**   | **160**               | **~138**                      |

This is consistent with BIZ-001's L2 expansion (20 sections, 3 groups) and PA-001's L2 (6 domains, 75+ content units).

---

## 6. Evidence Basis

| Design Element                | Evidence                                         |
| ----------------------------- | ------------------------------------------------ |
| All 8 components preserved    | COM-WP04-004 §4 — no obsolete components         |
| Entitlements added            | CAP-001 §2; PA-001 §4.4                          |
| Cost preview & approval added | PA-001 §4.4; CON-001 PH-002, PP-003              |
| Country configuration added   | PA-001 §4.4; BIZ-001 §11                         |
| Currency/tax added            | PA-001 §4.4 "tax rules per country"; BIZ-001 §11 |
| Invoicing/procurement added   | BIZ-001 §8                                       |
| Traceability tables added     | Pattern from PA-001/BIZ-001 §19-20               |
| Ownership boundary added      | Pattern from BIZ-001 §2                          |
| 9-part grouping               | Task brief §8 explicit grouping request          |

---
