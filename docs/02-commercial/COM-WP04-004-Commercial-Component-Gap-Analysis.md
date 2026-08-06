# COM-WP04-004 — Commercial Component Gap Analysis

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised

---

## 1. Purpose

This report assesses each current COM-001 component and identifies missing commercial concepts requiring expansion. Each item is grounded in authoritative evidence. No policy decisions are invented — unresolved items are flagged for the Founder Decision Agenda (COM-WP04-006).

---

## 2. Current Component Assessment

### 2.1 Credit Economy (Skeleton §5)

**Adequate? Partially.** Current content: Credits represent publishing capacity; must be transparent, auditable, support individuals and organisations, avoid hidden consumption; algorithms deferred.

| Gap                                     | Evidence                                                                                | Status                                                               |
| --------------------------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Credit acquisition (purchase flow)      | PA-001 §4.4 "Credit purchase — bundle selection, payment initiation, credit allocation" | **Missing**                                                          |
| Credit consumption rules                | PA-001 §4.4 "deduction on publish, output selection, page extension"                    | **Missing**                                                          |
| Non-expiry rule                         | BIZ-001 §16 "Purchased credits do not expire"; CON-001 PH-003                           | **Settled — must implement**                                         |
| Promotional credits                     | Legacy CP-006 (source material only) "Promotional credits may follow different rules"   | **Proposed** — Founder decision on whether promotional credits exist |
| Credit reversal / refunds / adjustments | PA-001 §4.4 "refund and adjustment handling (governed by COM-001 rules)"                | **Missing**                                                          |
| Minimum bundle                          | BIZ-001 §16 "introductory low-cost bundles"                                             | **Needs Founder decision**                                           |
| Credit denominations                    | BIZ-001 §16 "Bundle sizes range from introductory... through regular... to large"       | **Needs definition**                                                 |

### 2.2 Publication Output Model (Skeleton §6)

**Adequate? Partially.** Current content: Value tied to outputs; publishing events become commercial trigger.

| Gap                                     | Evidence                                                   | Status                                  |
| --------------------------------------- | ---------------------------------------------------------- | --------------------------------------- |
| Base publication cost model             | BIZ-001 §16 "base allowance" implied                       | **Needs Founder decision**              |
| Additional-page charging                | BIZ-001 §16 "extra pages beyond the base allowance"        | **Needs Founder decision**              |
| Output add-ons                          | BIZ-001 §16 branding removal, embeds, offline, self-hosted | **Needs expansion**                     |
| What is a "publication output"          | CON-001 PH-001 defines value by outputs; legacy CP-005     | **Needs precise commercial definition** |
| Republishing / post-publication changes | CON-001 PP-003 "publication replacement" context           | **Needs Founder decision**              |

### 2.3 Wallet & Ledger (Skeleton §7)

**Adequate? Partially.** Current content: Wallet records publishing capacity; ledger immutable history of acquisition, consumption, adjustments, refunds, administrative actions.

| Gap                                            | Evidence                                                                                    | Status                                            |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| Wallet ownership model                         | CAP-004 — Wallet business asset owned by Commercial                                         | **Needs definition** — who/what can hold a wallet |
| Wallet lifecycle                               | PA-001 §4.4 "creation, balance tracking, lifetime record"                                   | **Missing**                                       |
| Ledger immutability and auditability rules     | Skeleton §7 "immutable history"; legacy CP-008                                              | **Needs rule precision**                          |
| Cost preview before deduction                  | PA-001 §4.4 "cost preview — transparent display of costs before commitment"; CON-001 PH-002 | **Missing from skeleton**                         |
| User approval before consumption               | Legacy CP-003 (source); CON-001 PP-003 "costs visible before action"                        | **Needs authoritative embedding**                 |
| Wallet closure / inactive account with balance | Not addressed                                                                               | **Founder decision**                              |

### 2.4 Pricing Architecture (Skeleton §8)

**Adequate? Partially.** Current content: Pricing simple, scales with usage, supports segments, avoids complexity; specific price points maintained separately.

| Gap                                       | Evidence                                                                          | Status                                                  |
| ----------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------- |
| Pricing architecture vs strategy boundary | PA-001 §4.4 "Commercial must not define pricing strategy — COM-001 defines rules" | **Needs explicit boundary statement**                   |
| Base vs add-on separation                 | BIZ-001 §16 base allowance vs add-ons                                             | **Needs Founder decision**                              |
| Price-point governance                    | Skeleton §8 "specific price points maintained separately"                         | **Needs governance rule** — who sets prices and how     |
| Segment pricing                           | BIZ-001 §8 segments                                                               | **Needs expansion** — volume, institutional, enterprise |

### 2.5 Payment Strategy (Skeleton §9)

**Adequate? Partially.** Current content: Supports African payment ecosystems + international; provider selection deferred to implementation.

| Gap                     | Evidence                                                          | Status                                                                       |
| ----------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Payment method types    | BIZ-001 §11 mobile money, card, invoicing                         | **Needs expansion**                                                          |
| Country configuration   | PA-001 §4.4 "country-aware commercial configuration"; BIZ-001 §11 | **Needs framework**                                                          |
| Currency handling       | BIZ-001 §11 "currencies"                                          | **Needs rules framework**                                                    |
| Tax handling            | PA-001 §4.4 "tax rules per country"                               | **Needs rules framework**                                                    |
| Invoicing / procurement | BIZ-001 §8 government procurement                                 | **Needs expansion**                                                          |
| Provider abstraction    | PA-001 "Payment provider integration is an ARC-001 concern"       | **Boundary must be explicit** — COM-001 defines strategy, ARC-001 implements |

### 2.6 Organisation Commercial Model (Skeleton §10)

**Adequate? Partially.** Current content: Supports individuals, organisations, multi-user, delegated administration, shared commercial management.

| Gap                                    | Evidence                                                                                     | Status                                     |
| -------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------ |
| Organisation credit allocation         | BIZ-001 §6 "allocated credit pools"; §8 "allocate publishing capacity"                       | **Missing mechanics**                      |
| Subscriptions as recurring allocations | BIZ-001 §6 "monthly or annual credit allocations, consolidated billing"                      | **Needs mechanics**                        |
| Admin commercial controls              | CON-001 §8 Organisation Administrator "credit allocations, branding and commercial settings" | **Needs expansion**                        |
| Approvals                              | CON-001 §8 "may require approval before publishing"                                          | **Needs mechanics**                        |
| Subscriptions optional                 | CON-001 PH-003                                                                               | **Settled** — must preserve pay-per-output |

### 2.7 Publication Hosting Lifecycle (Skeleton §11)

**Adequate? Partially.** Current content: Activation, hosting duration, renewal, archival, retirement.

| Gap                                    | Evidence                                                               | Status                     |
| -------------------------------------- | ---------------------------------------------------------------------- | -------------------------- |
| Hosting duration                       | BIZ-001 §5 "defined hosting durations"; CON-001 §7.1 "defined periods" | **Needs Founder decision** |
| Renewal mechanics                      | BIZ-001 §16 "hosting renewal"; CON-001 PP-003 "hosting expiry"         | **Needs definition**       |
| Archival / retirement commercial terms | CON-001 §7.1 "clear renewal, archival and retirement rules"            | **Needs definition**       |
| Non-renewal consequences               | Not addressed                                                          | **Needs Founder decision** |

### 2.8 Commercial Governance Principles (Skeleton §12)

**Adequate? Partially.** Current content: Transparent, predictable, auditable, explainable, customer-centred.

| Gap                  | Evidence                                        | Status       |
| -------------------- | ----------------------------------------------- | ------------ |
| Traceability         | Missing entirely — no CAP/PA/BIZ/CON references | **Must add** |
| Ownership boundary   | Missing "owns/does not own"                     | **Must add** |
| Downstream consumers | Missing table                                   | **Must add** |

### 2.9 Commercial Decisions (Skeleton §14)

**Adequate? Partially.** Current content: 4 decisions — outputs = value unit; credits measure capacity; pricing transparent; commercial separable from technical.

| Gap                              | Evidence                                                                    | Status              |
| -------------------------------- | --------------------------------------------------------------------------- | ------------------- |
| Settled constitutional decisions | Non-expiry; subscriptions optional; Africa-first; organisations first-class | **Must codify**     |
| Founder decision gaps            | See COM-WP04-006                                                            | **Founder decides** |

---

## 3. Missing Concepts Requiring New Content

| Concept                                     | Evidence                                                                   | Type                                 |
| ------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------ |
| **Entitlements model**                      | CAP-001 §2 Commercial → Entitlements; PA-001 §4.4 "entitlement management" | Must add                             |
| **Cost preview / approval**                 | PA-001 §4.4; CON-001 PH-002, PP-003                                        | Must add                             |
| **Credit acquisition flow**                 | PA-001 §4.4                                                                | Must add                             |
| **Credit reversal / refund / adjustment**   | PA-001 §4.4                                                                | Must add                             |
| **Promotional credits**                     | Legacy CP-006 (source)                                                     | Founder decides whether to adopt     |
| **Country commercial configuration**        | PA-001 §4.4; BIZ-001 §11                                                   | Must add framework                   |
| **Currency & tax rules framework**          | PA-001 §4.4; BIZ-001 §11                                                   | Must add framework                   |
| **Invoicing / procurement**                 | BIZ-001 §8                                                                 | Must add                             |
| **Commercial exceptions**                   | Not currently addressed                                                    | Must add — governance for exceptions |
| **Inactive account with remaining credits** | Not addressed                                                              | Founder decision                     |
| **Revenue recognition boundary**            | BIZ-001 §16                                                                | Must respect — record as constraint  |

---

## 4. Structural Assessment

| Current component                | Verdict                                    |
| -------------------------------- | ------------------------------------------ |
| Credit Economy                   | Keep — expand                              |
| Publication Output Model         | Keep — expand                              |
| Wallet & Ledger                  | Keep — expand                              |
| Pricing Architecture             | Keep — expand                              |
| Payment Strategy                 | Keep — expand                              |
| Organisation Commercial Model    | Keep — expand                              |
| Hosting Lifecycle                | Keep — expand                              |
| Commercial Governance Principles | Keep — expand into full Governance section |
| Commercial Decisions             | Keep — expand into Foundational Decisions  |

**No component is obsolete or contradictory.** All components survive; each requires expansion. The proposed target structure (COM-WP04-007) regroups them preserving all existing content.

---

## 5. Gap Summary by Severity

| Severity                                           | Count | Examples                                                                                                                                                                                                                             |
| -------------------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Must add** (required by authoritative documents) | 12    | Entitlements, cost preview, credit acquisition, reversal/refund, country config, currency/tax framework, invoicing/procurement, ledger rules, traceability, ownership boundary, downstream consumers, revenue-recognition constraint |
| **Founder decision required** (not settled)        | 9     | Minimum bundle vs $1, inactive-account credits, base page allowance, additional-page pricing, hosting duration, renewal mechanics, add-on pricing mechanics, free-vs-chargeable actions, republishing consumption                    |

---
