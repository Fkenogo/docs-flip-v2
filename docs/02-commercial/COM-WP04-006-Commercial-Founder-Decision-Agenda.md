# COM-WP04-006 — Commercial Founder Decision Agenda

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised

---

## 1. Purpose

This agenda identifies the bounded Founder decisions required before COM-001 implementation. Each decision provides: issue, options, consequences, recommendation, evidence, and implementation dependency.

**The decisions are NOT made here. The Founder decides.**

The agenda also resolves the 13 specific questions from the task brief by classifying each as **Settled** (by authoritative documents) or **Requires Founder decision**.

---

## 2. Specific Question Classification

| #   | Question                                                                                 | Classification               | Basis / Decision Ref                                                                                            |
| --- | ---------------------------------------------------------------------------------------- | ---------------------------- | --------------------------------------------------------------------------------------------------------------- |
| 1   | Are purchased credits non-expiring?                                                      | **SETTLED — Yes**            | BIZ-001 §16 "Purchased credits do not expire"; CON-001 PH-003. COM-001 must implement non-expiry.               |
| 2   | How should long-inactive accounts holding credits be treated without confiscating value? | **FOUNDER DECISION — FD-01** | Not settled in any authoritative document.                                                                      |
| 3   | Is the minimum purchase bundle distinct from the "from as little as $1" proposition?     | **FOUNDER DECISION — FD-02** | BIZ-001 §16 states the proposition; mechanical distinction not defined.                                         |
| 4   | How are base publication costs and optional outputs separated?                           | **FOUNDER DECISION — FD-03** | BIZ-001 §16 implies base + add-ons; pricing mechanics not settled.                                              |
| 5   | What publication page allowance belongs in the base commercial model?                    | **FOUNDER DECISION — FD-04** | BIZ-001 §16 references "base allowance" but does not set it.                                                    |
| 6   | How are additional pages charged?                                                        | **FOUNDER DECISION — FD-05** | BIZ-001 §16 references "extra pages beyond the base allowance" without price mechanics.                         |
| 7   | What hosting duration is included?                                                       | **FOUNDER DECISION — FD-06** | CON-001 §7.1 "defined periods"; BIZ-001 §5 "defined hosting durations" — duration not set.                      |
| 8   | How are hosting renewals treated?                                                        | **FOUNDER DECISION — FD-07** | BIZ-001 §16 "hosting renewal"; CON-001 PP-003 "hosting expiry" — mechanics not settled.                         |
| 9   | How should republishing or post-publication changes consume credits?                     | **FOUNDER DECISION — FD-08** | CON-001 PP-003 "publication replacement" exists; consumption rules not settled.                                 |
| 10  | Which actions are free because they do not create a publication output?                  | **FOUNDER DECISION — FD-09** | Legacy CP-001 guiding rule (source material) supports output-based charging; no authoritative free-action list. |
| 11  | How should organisation subscriptions coexist with credit consumption?                   | **FOUNDER DECISION — FD-10** | BIZ-001 §6 confirms coexistence ("organisations still see how credits are consumed") but mechanics not settled. |
| 12  | How should enterprise procurement, invoicing and negotiated arrangements be represented? | **FOUNDER DECISION — FD-11** | BIZ-001 §6/§8 establish the arrangement exists; representation mechanics not settled.                           |
| 13  | Which commercial concerns belong in COM-001 vs future PRC-001/PAY-001/PUB-001?           | **RECOMMENDATION ONLY**      | COM-WP04-005 recommends all three remain candidates; COM-001 absorbs the content first. Founder confirms.       |

---

## 3. Founder Decision Agenda

### FD-01 — Inactive-Account Credit Treatment

| Element                       | Detail                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | Long-inactive accounts may hold purchased credits. COM-001 must define whether, when, and how such credits are treated — without confiscating customer value (CON-001 PH-003: "return months later and publish again").                                                                                                                                                                                                                       |
| **Options**                   | A) Non-expiring indefinitely, inactive or not (value never confiscated; deferred revenue held indefinitely). B) Non-expiring but account enters dormant status with communication obligations and no service change. C) Non-expiring with a defined extended-inactivity reconciliation process requiring explicit customer confirmation. D) Expiry after a defined period (conflicts with BIZ-001 "do not expire" — likely unconstitutional). |
| **Consequences**              | A maximises trust and PH-003 compliance but carries long-dated deferred-revenue liability. B/C preserve value while managing account hygiene. D violates BIZ-001 §16 and CON-001 PH-003.                                                                                                                                                                                                                                                      |
| **Recommendation**            | Option C — non-expiry preserved; dormant-state communication and explicit reconciliation; no value confiscation.                                                                                                                                                                                                                                                                                                                              |
| **Evidence**                  | CON-001 PH-003, PP-003; BIZ-001 §16 "Purchased credits do not expire"; BIZ-001 §16 "unused credits represent deferred revenue, not lost revenue".                                                                                                                                                                                                                                                                                             |
| **Implementation dependency** | Required before COM-001 Credit and Wallet sections can be written.                                                                                                                                                                                                                                                                                                                                                                            |

### FD-02 — Minimum Purchase Bundle vs "$1 Publication Proposition"

| Element                       | Detail                                                                                                                                                                                                                                                                                              |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | BIZ-001 §16 states "from as little as $1" as an accessibility proposition "without requiring every transaction to be $1". COM-001 must define the mechanical relationship between a minimum purchase bundle and the per-publication cost.                                                           |
| **Options**                   | A) Minimum bundle equals the lowest-cost publication (bundle = one publication at ~$1 equivalent). B) Minimum bundle is higher than the lowest publication cost, allowing "from as little as $1" per publication within a bundle. C) No formal minimum bundle; any credit denomination purchasable. |
| **Consequences**              | A simplifies but may undercut bundle economics. B preserves the marketing proposition while maintaining a viable minimum transaction. C maximises flexibility but may complicate payment-minimum realities in some markets.                                                                         |
| **Recommendation**            | Option B — bundle floor with per-publication costs below the bundle floor, enabling the "$1 publication" within a purchased bundle.                                                                                                                                                                 |
| **Evidence**                  | BIZ-001 §16 Revenue Principles; COM-001 §6 Publication Output Model.                                                                                                                                                                                                                                |
| **Implementation dependency** | Required before Credit Economy and Pricing Architecture sections.                                                                                                                                                                                                                                   |

### FD-03 — Base vs Optional Output Separation

| Element                       | Detail                                                                                                                                                                                                                                                                                                                                                |
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | COM-001 must define the boundary between base publication cost (included in a publish action) and optional outputs (purchased add-ons).                                                                                                                                                                                                               |
| **Options**                   | A) Base = a hosted publication with standard page allowance and standard sharing (links); optionally priced: branding removal, embeds, offline packages, self-hosted, advanced analytics. B) Base = publication only; every distribution channel priced. C) Base = publication with all standard distribution; only premium/advanced features priced. |
| **Consequences**              | A aligns with BIZ-001 §5 "Self-Service Publishing Platform" (links, embeds, QR standard) and §16 add-ons. B would price standard sharing, conflicting with the core publishing proposition. C adds complexity to the base.                                                                                                                            |
| **Recommendation**            | Option A — base publication includes hosting + standard share links; add-ons are optional purchases.                                                                                                                                                                                                                                                  |
| **Evidence**                  | BIZ-001 §5 (value delivery: links, embeds, QR); BIZ-001 §16 (add-ons listed as additions); PA-001 §4.3.3 (Distribution standard); CON-001 PH-005 (simplicity).                                                                                                                                                                                        |
| **Implementation dependency** | Required before Publication Output Model expansion.                                                                                                                                                                                                                                                                                                   |

### FD-04 — Base Page Allowance

| Element                       | Detail                                                                                                                                                                                        |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | BIZ-001 §16 references "extra pages beyond the base allowance" implying a base page allowance. COM-001 must define what the base allowance is.                                                |
| **Options**                   | A) Fixed base page count (e.g., 50 pages) with additional-page pricing beyond. B) Tiered by publication type/size. C) Unlimited pages in base (no page model).                                |
| **Consequences**              | A is simple (PH-005) and matches BIZ-001's "base allowance" language. B adds tier complexity. C removes BIZ-001's page-charging revenue dimension and conflicts with "extra pages" reference. |
| **Recommendation**            | Option A — a single fixed base page allowance, kept simple. Specific number is a price point (maintained separately per COM-001 §8) but the allowance structure is architectural.             |
| **Evidence**                  | BIZ-001 §16 "extra pages beyond the base allowance"; CON-001 PH-005 (simplicity).                                                                                                             |
| **Implementation dependency** | Required before Publication Output Model expansion.                                                                                                                                           |

### FD-05 — Additional-Page Charging

| Element                       | Detail                                                                                                                                   |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | BIZ-001 §16 references charging for "extra pages". COM-001 must define the charging mechanics.                                           |
| **Options**                   | A) Per-page block charging (e.g., per additional block of pages). B) Per-individual-page charging. C) Page count tier upgrades.          |
| **Consequences**              | A balances granularity with simplicity. B maximises precision but adds pricing noise. C re-introduces tier complexity (PH-005 conflict). |
| **Recommendation**            | Option A — additional pages charged in defined blocks. Block size is a price point.                                                      |
| **Evidence**                  | BIZ-001 §16 "extra pages beyond the base allowance"; PA-001 §4.4 "page extension" as credit consumption; CON-001 PH-005.                 |
| **Implementation dependency** | Required before Publication Output Model expansion.                                                                                      |

### FD-06 — Included Hosting Duration

| Element                       | Detail                                                                                                                                                                                                                                               |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | CON-001 §7.1: hosting "for defined periods, with clear renewal, archival and retirement rules". BIZ-001 §5: "defined hosting durations". The duration itself is not settled.                                                                         |
| **Options**                   | A) Fixed initial hosting duration (e.g., 12 months) included in base publication cost, with renewal thereafter. B) Duration tied to subscription term. C) Perpetual hosting included (conflicts with "defined periods" and hosting-renewal revenue). |
| **Consequences**              | A matches the "defined periods" language and creates a clear renewal event. B works only for subscribers and conflicts with pay-per-output independence. C contradicts CON-001 §7.1 and BIZ-001 §16 "hosting renewal" revenue.                       |
| **Recommendation**            | Option A — a defined initial hosting period included in the base output; renewal thereafter. Specific duration is a commercial parameter subject to Founder approval as a price point.                                                               |
| **Evidence**                  | CON-001 §7.1 "defined periods"; BIZ-001 §5 "defined hosting durations"; BIZ-001 §16 "hosting renewal".                                                                                                                                               |
| **Implementation dependency** | Required before Hosting Lifecycle expansion.                                                                                                                                                                                                         |

### FD-07 — Hosting Renewal Treatment

| Element                       | Detail                                                                                                                                                                                                                                                                         |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Issue**                     | COM-001 must define how hosting renewal works commercially: renewal window, what happens on non-renewal, pricing basis.                                                                                                                                                        |
| **Options**                   | A) Renewable in fixed increments; non-renewal transitions publication to archived state per defined rules. B) Auto-renew cleared by credits; non-renewal leads to archival after grace period. C) No renewal — one-time hosting only (conflicts with CON-001's renewal model). |
| **Consequences**              | A gives publishers control (CON-001 PP-004). B risks surprising consumption (PP-003 transparency). C eliminates the hosting-renewal revenue dimension in BIZ-001 §16.                                                                                                          |
| **Recommendation**            | Option A — explicit renewal with prior notification and transparent pricing (PP-003); non-renewal leads to archival per defined rules.                                                                                                                                         |
| **Evidence**                  | CON-001 PP-003 (hosting expiry visible before action), PP-004 (user control), §7.1; BIZ-001 §16 "hosting renewal".                                                                                                                                                             |
| **Implementation dependency** | Required before Hosting Lifecycle expansion.                                                                                                                                                                                                                                   |

### FD-08 — Republishing / Post-Publication Changes

| Element                       | Detail                                                                                                                                                                                                                                                                                                                           |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | CON-001 PP-003 references "publication replacement". COM-001 must define whether updating or replacing a publication consumes credits.                                                                                                                                                                                           |
| **Options**                   | A) Any publish-output action (including re-publish/replace) consumes credits — aligned with output-based value. B) Post-publish changes within a defined window and within page allowance are free; page-increasing changes consume credits. C) All updates free (conflicts with output-based value; BIZ-001 revenue alignment). |
| **Consequences**              | A is the purest output-based model but may penalise corrections. B balances transparency with publishing flexibility. C undermines the revenue model.                                                                                                                                                                            |
| **Recommendation**            | Option B — a defined post-publication free-correction window for non-material changes; material changes (page increases, new outputs) consume credits.                                                                                                                                                                           |
| **Evidence**                  | CON-001 PP-003 "publication replacement" transparency; BIZ-001 §16 "revenue recognition occurs at credit consumption"; CON-001 PP-005 flexible publishing.                                                                                                                                                                       |
| **Implementation dependency** | Required before Publication Output Model expansion.                                                                                                                                                                                                                                                                              |

### FD-09 — Free vs Chargeable Actions

| Element                       | Detail                                                                                                                                                                                                                                                                                              |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | COM-001 must define which actions are free because they create no publication output. Legacy CP-001 guides: "If there is no meaningful publication output, the action should normally not consume credits."                                                                                         |
| **Options**                   | A) Free (no credit consumption): account creation, upload, preview, draft saving, sharing metadata editing within allowance, analytics viewing (basic). Charged: publish, page increases, output add-ons, hosting renewal. B) Free list shorter/mixed. C) Free list longer to include some add-ons. |
| **Consequences**              | A matches the output-based constitutional principle and CP-001. B/C distort the model.                                                                                                                                                                                                              |
| **Recommendation**            | Option A — explicit free-actions list grounded in "no publication output created"; chargeable list grounded in "publication output or renewal created".                                                                                                                                             |
| **Evidence**                  | Legacy CP-001 "Pay for Outputs" (source); CON-001 PH-001, PP-002; PA-001 §4.4 (credit consumption on publish; failure handling not on preview).                                                                                                                                                     |
| **Implementation dependency** | Required before Credit Consumption rules.                                                                                                                                                                                                                                                           |

### FD-10 — Organisation Subscription / Credit Coexistence

| Element                       | Detail                                                                                                                                                                                                                                                                                                                                                              |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | BIZ-001 §6: subscriptions "maintain the credit-based consumption model — organisations still see how credits are consumed". COM-001 must define the coexistence mechanics.                                                                                                                                                                                          |
| **Options**                   | A) Subscription deposits credits into an organisational wallet each period; consumption identical to individual credits; subscription is a funding mechanism, not a different consumption model. B) Subscription grants entitlement to a fixed publication volume per period without wallet credits. C) Hybrid: subscription credits + additional bundle purchases. |
| **Consequences**              | A preserves a single credit model (simplicity, transparency) and matches BIZ-001's "credit-based consumption". B diverges into two consumption systems. C adds complexity but enterprise flexibility.                                                                                                                                                               |
| **Recommendation**            | Option A — subscriptions are credit-funded organisational wallets; single consumption model. Option C may be added later for enterprise if evidence demands.                                                                                                                                                                                                        |
| **Evidence**                  | BIZ-001 §6 "subscriptions... maintaining the credit-based consumption model"; CON-001 PP-007; PH-005 simplicity.                                                                                                                                                                                                                                                    |
| **Implementation dependency** | Required before Organisation Commercial Model expansion and Wallet/Entitlements.                                                                                                                                                                                                                                                                                    |

### FD-11 — Enterprise Procurement Representation

| Element                       | Detail                                                                                                                                                                                                                                                                                                   |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | BIZ-001 §6/§8 establish enterprise arrangements (custom pricing, invoicing, volume commitments). COM-001 must define how these are represented commercially.                                                                                                                                             |
| **Options**                   | A) Enterprise is an overlay on the standard model: negotiated contracts set credit pricing/volumes; invoicing replaces card/mobile-money payment for the organisation's wallet top-ups. B) Separate enterprise product with distinct commercial rules. C) Defer entirely to a later specialist document. |
| **Consequences**              | A keeps one commercial engine with negotiated parameters. B creates a parallel model and maintenance burden. C leaves the requirement unmet in COM-001.                                                                                                                                                  |
| **Recommendation**            | Option A — enterprise arrangements as negotiated overlays on the standard credit/wallet model, with invoicing/procurement as payment channels.                                                                                                                                                           |
| **Evidence**                  | BIZ-001 §6 "custom pricing, volume commitments, invoicing", §8 "procurement-compatible payment"; CON-001 PP-007 organisation-first.                                                                                                                                                                      |
| **Implementation dependency** | Required before Payments and Organisation Commercial Model sections.                                                                                                                                                                                                                                     |

### FD-12 — Price-Point Governance (derived, not in 13 questions)

| Element                       | Detail                                                                                                                                                                                                                                               |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Issue**                     | COM-001 §8 says "Specific price points are maintained separately from this document." COM-001 must define who governs price points and how they change.                                                                                              |
| **Options**                   | A) Price points are Founder-approved commercial parameters; COM-001 defines architecture and governance, not the numbers. B) Price points defined in COM-001 directly. C) Price points delegated to operational documents without Founder oversight. |
| **Consequences**              | A matches BIZ-001's separation of strategy (BIZ-001) / architecture (COM-001) / price points (maintained separately) and keeps constitutional stability. B inverts the skeleton's own statement. C loses Founder control.                            |
| **Recommendation**            | Option A — COM-001 defines pricing architecture and the governance rule; price points are Founder-approved values maintained outside COM-001.                                                                                                        |
| **Evidence**                  | COM-001 §8 "Specific price points are maintained separately"; PA-001 §4.4 "Commercial must not define pricing strategy — COM-001 defines rules"; MP-001 constitutional governance pattern.                                                           |
| **Implementation dependency** | Required before Pricing Architecture expansion.                                                                                                                                                                                                      |

---

## 4. Decision Summary Table

| Ref   | Decision                              | Settled?                          | Needed For              |
| ----- | ------------------------------------- | --------------------------------- | ----------------------- |
| FD-01 | Inactive-account credit treatment     | No                                | Credit + Wallet         |
| FD-02 | Minimum bundle vs $1 proposition      | No                                | Credit + Pricing        |
| FD-03 | Base vs optional output separation    | No                                | Output Model            |
| FD-04 | Base page allowance                   | No                                | Output Model            |
| FD-05 | Additional-page charging              | No                                | Output Model            |
| FD-06 | Included hosting duration             | No                                | Hosting Lifecycle       |
| FD-07 | Hosting renewal treatment             | No                                | Hosting Lifecycle       |
| FD-08 | Republishing consumption              | No                                | Output Model            |
| FD-09 | Free vs chargeable actions            | No                                | Credit Consumption      |
| FD-10 | Subscription/credit coexistence       | No                                | Organisation + Wallet   |
| FD-11 | Enterprise procurement representation | No                                | Payments + Organisation |
| FD-12 | Price-point governance                | No                                | Pricing Architecture    |
| Q1    | Non-expiring credits                  | **Yes**                           | Credit                  |
| Q11   | Subscriptions optional                | **Yes**                           | Organisation            |
| Q13   | COM-001 vs PRC/PAY/PUB scope          | **Recommendation** (COM-WP04-005) | Structural              |

---

## 5. Settled Constitutional Constraints COM-001 Must Implement

| Constraint                                       | Source                                           |
| ------------------------------------------------ | ------------------------------------------------ |
| Purchased credits do not expire                  | CON-001 PH-003; BIZ-001 §16                      |
| Subscriptions never the only way to publish      | CON-001 §7.2; PH-003                             |
| Revenue recognition at credit consumption        | BIZ-001 §16                                      |
| Credit consumption only for publication outputs  | CON-001 PH-001, PP-002; BIZ-001 §6               |
| Costs visible before commitment                  | CON-001 PH-002, PP-003; PA-001 §4.4 cost preview |
| Africa-first commercial design                   | CON-001 PH-006, PP-009; BIZ-001 §11              |
| Organisations first-class                        | CON-001 PH-007, PP-007; BIZ-001 §6, §8           |
| Per-publication margin positive at lowest bundle | BIZ-001 §15                                      |
| No new Level 1 capabilities                      | CAP-005; MP-001 Operating Rule 8                 |

---

## 6. Decision Implementation Dependency

COM-001 **cannot be fully written** until the 12 Founder decisions are made. The recommended ordering:

1. **Blocking, first tranche** (needed for core sections): FD-02, FD-03, FD-04, FD-05, FD-09
2. **Second tranche** (needed for hosting/wallet): FD-06, FD-07, FD-08
3. **Third tranche** (needed for organisation/enterprise/pricing): FD-10, FD-11, FD-12, FD-01

The Loop 1 (Structure Alignment) can proceed with settled constraints only. Loop 2 (Content Expansion) requires the Founder decisions.

---
