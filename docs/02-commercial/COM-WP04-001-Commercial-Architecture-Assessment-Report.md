# COM-WP04-001 — Commercial Architecture Assessment Report

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised  
**Document Assessed:** DOCSFLIP-COM-001 v0.1 (L1 — Skeleton)

---

## 1. Current Purpose and Scope

COM-001 v0.1 states its purpose as: "This document defines the commercial operating model of Docsflip. It translates the business model into concrete commercial rules without describing technical implementation. It is the authoritative source for how value is measured, charged, purchased and managed."

The scope is appropriately bounded: it excludes technical implementation (delegated to ARC-001) and business strategy (owned by BIZ-001). The commercial philosophy section (5 principles) aligns with the constitutional principles.

## 2. Strengths

| Strength                                     | Evidence                                                                                   |
| -------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Correct architectural positioning            | Header now reads `PA-001 (architectural); BIZ-001 (content)` post-reconciliation           |
| Purpose correctly distinguishes from BIZ-001 | "translates the business model into concrete commercial rules"                             |
| Commercial principles aligned with CON-001   | Pay for outcomes, transparency, publish when needed, revenue/value alignment, Africa-first |
| Clear commercial components list             | 8 components identified in §4                                                              |
| Governance principles present                | §12 — transparent, predictable, auditable, explainable, customer-centred                   |
| Technical separation maintained              | "Detailed algorithms remain implementation concerns" (§5)                                  |
| Provider selection deferred                  | "Provider selection is an implementation decision" (§9) — correctly defers to ARC-001      |
| Legacy source properly separated             | Legacy COM-001 marked non-authoritative                                                    |

## 3. Structural Weaknesses

| Weakness                            | Detail                                                                                                                                                                               |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Maturity overstates position**    | Label L1 — Skeleton is accurate but the content is thin relative to the task — only 14 sections, most 1-4 sentences. The skeleton is a **starting shell**, not a complete framework. |
| **No traceability section**         | §13 lists relationships but does not trace components to CAP-001/002, PA-001, BIZ-001, or CON-001 principles                                                                         |
| **No capability mapping**           | No explicit mapping of the 8 components to the Commercial capability decomposition                                                                                                   |
| **No business-asset ownership**     | Wallet, Credit, Payment assets from CAP-004 are not allocated to COM-001 components                                                                                                  |
| **No downstream-consumer table**    | Unlike PA-001/BIZ-001 which have explicit "Downstream Consumers" tables                                                                                                              |
| **No constitutional citations**     | No explicit PH/PP references (the skeleton says "align with customer value" but doesn't cite CON-001 PH-001/PP-002)                                                                  |
| **No ownership boundary statement** | No "COM-001 owns / COM-001 does not own" section (BIZ-001 has this pattern; COM-001 lacks it)                                                                                        |

## 4. Missing Commercial Components

| Missing Component                        | Evidence of Need                                                                                                  |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Credit acquisition (purchase flow)       | PA-001 §4.4 lists as primary responsibility; not in skeleton                                                      |
| Credit consumption rules                 | PA-001 §4.4 — "deduction on publish, output selection, page extension"                                            |
| Cost preview / customer approval         | PA-001 §4.4 primary responsibility; PH-002/PP-003                                                                 |
| Credit reversal / refunds / adjustments  | PA-001 §4.4 — "refund and adjustment handling (governed by COM-001 rules)"                                        |
| Wallet ownership model                   | CAP-004 — Wallet asset; not defined in skeleton                                                                   |
| Organisation credit allocation           | BIZ-001 §8 — allocated credit pools; skeleton §10 mentions "shared commercial management" but no allocation rules |
| Publication entitlements                 | PA-001 §4.4 — "what a user/organisation can do based on credits held"                                             |
| Output add-ons                           | BIZ-001 §16 — branding removal, embeds, offline packages, self-hosted, hosting renewal                            |
| Hosting renewal rules                    | Skeleton §11 mentions renewal but no rules                                                                        |
| Inactive account / remaining credits     | Not addressed anywhere; requires Founder decision                                                                 |
| Tax / currency / payment-market concerns | BIZ-001 §11 — country configuration; PA-001 §4.4 — "country-aware commercial configuration"                       |
| Enterprise invoicing / procurement       | BIZ-001 §8 — government segment requires procurement-compatible payment                                           |
| Commercial exceptions                    | Not addressed                                                                                                     |
| Revenue recognition boundaries           | BIZ-001 §16 — "revenue recognition occurs at credit consumption"; COM-001 must respect this boundary              |

## 5. Duplicated Concepts

No material duplication was found between COM-001 and BIZ-001 or PA-001. The separation is clean:

- BIZ-001 owns revenue _strategy_ and _model_.
- PA-001 owns the Commercial _capability/domain_.
- COM-001 owns commercial _mechanics and rules_.

## 6. Outdated Terminology

| Term                                | Status                                                                                                                                                |
| ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| "pay-as-you-publish"                | Consistent with BIZ-001 and CON-001                                                                                                                   |
| "credits"                           | Consistent                                                                                                                                            |
| "organisation accounts"             | BIZ-001 uses "organisation subscriptions" and "workspaces"; "organisation accounts" is acceptable but should align to "Organisation Commercial Model" |
| No legacy terminology contamination | Legacy CP-001–CP-010 are not in the authoritative skeleton (they are in the legacy file only)                                                         |

## 7. Incomplete Ownership Boundaries

| Gap                                      | Detail                                                                                                                                                                                                 |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| No "COM-001 owns / does not own" section | BIZ-001 §2 establishes this pattern; COM-001 lacks it                                                                                                                                                  |
| Pricing strategy ownership               | PA-001 §4.4 says "Commercial must not define pricing strategy — COM-001 defines rules" — but COM-001 must clarify it owns pricing _architecture_ while specific price points are maintained separately |
| Payment provider selection               | Correctly deferred to ARC-001 in §9                                                                                                                                                                    |

## 8. Missing Traceability

| Gap                                        | Detail                                                                                             |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| No CAP-001 traceability                    | Should map to Commercial capability (Wallet, Credits, Payments, Entitlements, Publication Outputs) |
| No CAP-002 traceability                    | Should map to the CAP-002 Commercial decomposition                                                 |
| No CAP-004 traceability                    | Should reference Wallet, Credit, Payment assets                                                    |
| No PA-001 traceability                     | Should reference PA-001 §4.4 Commercial domain                                                     |
| No BIZ-001 content-dependency traceability | Should state which BIZ-001 content it elaborates                                                   |
| No CON-001 constitutional traceability     | Should cite PH-001/002/003, PP-001/002/003/005/009                                                 |

## 9. Maturity Accuracy

**L1 — Skeleton is accurate.** The document is a shell of 14 short sections. It is not yet L2. Its current content is consistent and correctly positioned, but it lacks the depth, traceability, and ownership boundaries required for L2 — Expanded.

---

## 10. Assessment Summary

| Dimension                         | Verdict                                                                   |
| --------------------------------- | ------------------------------------------------------------------------- |
| Purpose & scope                   | Correct — needs sharper boundary statement                                |
| Constitutional alignment          | Good direction — needs explicit PH/PP citations                           |
| Capability alignment              | Implicit — needs explicit CAP-001/002/004 mapping                         |
| Business-model content dependency | Correct — needs explicit BIZ-001 input mapping                            |
| Component coverage                | Partial (8 components) — needs expansion to full commercial surface       |
| Traceability                      | Missing — needs constitutional, capability, domain, and downstream tables |
| Ownership boundaries              | Missing — needs owns/does-not-own statement                               |
| Maturity                          | L1 accurate — target L2 post-expansion                                    |

---
