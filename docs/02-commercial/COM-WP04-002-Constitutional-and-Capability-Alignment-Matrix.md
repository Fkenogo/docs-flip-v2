# COM-WP04-002 — Constitutional and Capability Alignment Matrix

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised

---

## 1. Constitutional Alignment — CON-001 Principles

| CON-001 Principle                                         | Core Requirement                                          | COM-001 Coverage (Current)                                                                   | Gap                            | Proposed COM-001 Grounding                                                                                 |
| --------------------------------------------------------- | --------------------------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| PH-001 — Publishing Outcomes Define Value                 | Value measured by published outcomes                      | §3 "pay-as-you-publish"; §6 "value tied to publication outputs"                              | Partial — no explicit citation | State PH-001 as commercial constitutional basis. Every commercial rule must trace to a publication output. |
| PH-002 — Transparency Is a Product Feature                | Costs/limits visible before commitment                    | §2 "Keep pricing transparent"; §5 "avoid hidden consumption"; §12 "transparent, predictable" | No explicit citation           | Cite PH-002. Embed cost-preview and pre-commitment disclosure as commercial requirements.                  |
| PH-003 — Access Should Not Require Unnecessary Commitment | Publish and leave without penalty; subscriptions optional | §3 "not through mandatory recurring subscriptions"                                           | No explicit citation           | Cite PH-003. Non-expiring credits and optional-subscription design must be constitutional.                 |
| PH-005 — Simplicity Outperforms Feature Accumulation      | Simple over complex                                       | §8 "avoid unnecessary complexity"                                                            | No explicit citation           | Cite PH-005. Pricing architecture must not accumulate tiers/complexity.                                    |
| PH-006 — Africa Is a Design Assumption                    | Payment/pricing designed for Africa first                 | §2 "Design for African purchasing realities"; §9 "African payment ecosystems"                | No explicit citation           | Cite PH-006. Country-aware configuration is constitutional.                                                |
| PP-001 — Publication-First                                | Decisions serve publishing outcomes                       | Implicit in §6                                                                               | Implicit                       | Align directly to PH-001/PP-001.                                                                           |
| PP-002 — Pay for Value Delivered                          | Charge for output, not access                             | §2 "Pay for publishing outcomes, not platform access"; §6                                    | Present but uncited            | Cite PP-002. Credit consumption tied to outputs only.                                                      |
| PP-003 — Transparency by Design                           | Costs visible before action                               | §12                                                                                          | Partial                        | Cite PP-003. Cost preview and ledger as design requirements.                                               |
| PP-005 — Flexible Publishing                              | Occasional and frequent publishers served                 | §2 "Allow organisations to publish when needed"; §3                                          | Present but uncited            | Cite PP-005. Commercial structure must serve once-a-year and daily publishers.                             |
| PP-007 — Organisation-Ready                               | Organisations natural extension                           | §10 "multi-user accounts; shared commercial management"                                      | Present but uncited            | Cite PP-007. Organisation commercial model is core, not upsell.                                            |
| PP-009 — Market-Aware                                     | African defaults                                          | §9                                                                                           | Present but uncited            | Cite PP-009. Payment-method and pricing defaults favour Africa.                                            |

**Assessment:** All constitutional principles that constrain the commercial model are **implicitly present** in the skeleton but **zero have explicit citations**. The skeleton demonstrates directional alignment but lacks constitutional traceability. COM-001 expansion must add explicit PH/PP citations for every commercial component.

**No conflicts detected** between the skeleton's principles and CON-001.

---

## 2. Capability Alignment — CAP-001 Commercial Capability

| CAP-001 Commercial Sub-capability | CAP-002 Mapping     | COM-001 Component (Current) | Assessment                                                                  |
| --------------------------------- | ------------------- | --------------------------- | --------------------------------------------------------------------------- |
| Wallet                            | Wallet              | §7 Wallet & Ledger          | Present — needs expansion to ownership, balances, ledger immutability rules |
| Credits                           | Credits             | §5 Credit Economy           | Present — needs acquisition, consumption, non-expiry, promotional rules     |
| Payments                          | Payments            | §9 Payment Strategy         | Present — needs purchase initiation, provider abstraction, payment methods  |
| Entitlements                      | Entitlements        | (absent)                    | **Missing** — needs what credits allow (publish, renew, add-ons)            |
| Publication Outputs               | Publication Outputs | §6 Publication Output Model | Present — needs base publication + add-ons + page/block model               |

**Assessment:** 4 of 5 CAP-001 Commercial sub-capabilities have a corresponding skeleton section. **Entitlements is missing.** COM-001 expansion must add an Entitlements model connecting credits to publication capability.

---

## 3. Business Asset Ownership — CAP-004

| CAP-004 Business Asset | Owner Capability | COM-001 Role                                                   | Assessment                                                     |
| ---------------------- | ---------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| Wallet                 | Commercial       | COM-001 defines wallet rules; PA-001 §4.4 owns the domain      | COM-001 must define wallet behaviour, balances, freeze/closure |
| Credit                 | Commercial       | COM-001 defines credit rules                                   | COM-001 must define credit life-cycle, non-expiry, reversal    |
| Payment                | Commercial       | COM-001 defines payment strategy; ARC-001 implements providers | COM-001 must define payment strategy, not provider selection   |

**Assessment:** COM-001 is the rules-owner for the three Commercial-owned business assets (Wallet, Credit, Payment). It must reference CAP-004 explicitly and defer asset _models/entities_ to DAT-001.

---

## 4. Domain Alignment — PA-001 Commercial Domain

| PA-001 §4.4 Element                                                   | COM-001 Responsibility                                                  | Assessment            |
| --------------------------------------------------------------------- | ----------------------------------------------------------------------- | --------------------- |
| Wallet management — creation, balance, lifetime record                | COM-001 defines wallet rules                                            | Needs expansion       |
| Credit purchase — bundle, payment initiation, allocation              | COM-001 defines bundle rules; payment initiation flows through Payments | Needs expansion       |
| Credit consumption — publish, output selection, page extension        | COM-001 defines what consumes credits and how much                      | Needs expansion       |
| Cost preview (PH-002)                                                 | COM-001 defines pre-commitment disclosure                               | Needs expansion       |
| Entitlement management                                                | COM-001 defines what credits allow                                      | Missing               |
| Publication output pricing                                            | COM-001 defines base + add-on pricing architecture                      | Needs expansion       |
| Transaction history — immutable ledger                                | COM-001 defines ledger rules                                            | Needs expansion       |
| Country configuration — payment, currency, tax                        | COM-001 defines country-commercial configuration                        | Needs expansion       |
| Refund and adjustment handling                                        | COM-001 defines rules                                                   | Missing from skeleton |
| "Commercial must not define pricing strategy — COM-001 defines rules" | COM-001 defines pricing _architecture_ and _rules_, not strategy        | Clarify boundary      |

**Assessment:** PA-001 §4.4 already specifies the full commercial surface COM-001 must define. The skeleton covers ~half.

---

## 5. Capability Creation Check

**COM-001 invents no new Level 1 capabilities.** Its scope is strictly the Commercial capability (CAP-001 §2). No new L1 capability is proposed. This complies with CAP-005 §"Introducing a New Capability" and MP-001 Operating Rule 8.

---

## 6. Summary Matrix

| Source                             | Alignment Status | Gap                              |
| ---------------------------------- | ---------------- | -------------------------------- |
| CON-001 PH-001/002/003/005/006     | Directional only | No citations                     |
| CON-001 PP-001/002/003/005/007/009 | Directional only | No citations                     |
| CAP-001 Commercial                 | Partial (4/5)    | Entitlements missing             |
| CAP-002 Commercial                 | Partial          | Needs full decomposition mapping |
| CAP-004 Wallet/Credit/Payment      | Implicit         | No asset-level references        |
| PA-001 §4.4 Commercial domain      | Partial (~50%)   | Needs full surface coverage      |
| New L1 capability creation         | None             | Compliant                        |

---
