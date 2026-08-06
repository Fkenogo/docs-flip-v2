# COM-WP04-003 — Business-to-Commercial Mapping Report

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised

---

## 1. Purpose

This report maps the approved business-model content (BIZ-001) into the commercial mechanics that COM-001 must define. It distinguishes **business strategy owned by BIZ-001** from **commercial mechanics owned by COM-001**, per the accepted dependency interpretation (architectural peers; content dependency BIZ-001 → COM-001).

---

## 2. BIZ-001 Content Dependency Map

### 2.1 Value Capture (§6)

| BIZ-001 Input                                   | BIZ-001 States                                                                                         | COM-001 Must Define (Mechanics)                                                                         | Ownership                                                  |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| Pay-Per-Publication (primary revenue mechanism) | "Customers purchase Docsflip Credits in bundles and consume them when they create publication outputs" | Credit consumption rules; publication output pricing; cost-per-output model                             | BIZ-001: revenue model. COM-001: mechanics.                |
| Revenue recognition at credit consumption       | "Revenue is recognised at the point of credit consumption"                                             | COM-001 must define the commercial event triggering consumption; revenue-recognition boundary respected | BIZ-001 sets the principle; COM-001 must not contradict it |

### 2.2 Credit Bundle Purchases (§6, §16)

| BIZ-001 Input                        | BIZ-001 States                                                                                   | COM-001 Must Define (Mechanics)                                            | Ownership                                                             |
| ------------------------------------ | ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| Bundle sizes by publishing frequency | "small bundles for occasional, larger for regular, allocated credit pools for organisational"    | Bundle architecture; minimum bundle; credit denominations                  | BIZ-001: segment intent. COM-001: bundle mechanics.                   |
| Purchased credits do not expire      | "Purchased credits do not expire merely because time has passed" (PH-003, PP-002)                | Non-expiry rule; promotional-credit exceptions; inactive-account treatment | **Settled by BIZ-001 + CON-001** — COM-001 must implement, not decide |
| "from as little as $1" proposition   | §16 Revenue Principles — communicates accessibility without requiring every transaction to be $1 | Minimum purchase bundle vs publication proposition distinction             | **Founder decision required** (see Q3 of Decision Agenda)             |

### 2.3 Organisation Subscriptions (§6, §8, §16)

| BIZ-001 Input                                                         | BIZ-001 States                                               | COM-001 Must Define (Mechanics)                                                     | Ownership                                                             |
| --------------------------------------------------------------------- | ------------------------------------------------------------ | ----------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| Subscriptions provide recurring credit allocations                    | "monthly or annual credit allocations, consolidated billing" | Subscription term, allocation mechanics, renewal, coexistence with consumed credits | BIZ-001: subscription model. COM-001: mechanics.                      |
| Organisation sees credit consumption by publication/member/department | §6 "organisations still see how credits are consumed"        | Organisation-level credit allocation, reporting, allocation rules                   | BIZ-001: transparency requirement. COM-001: allocation mechanics.     |
| Subscriptions optional                                                | CON-001 PH-003; BIZ-001 §16                                  | Subscription must never be the only way to publish                                  | Constitutional constraint — COM-001 must preserve pay-per-output path |

### 2.4 Publication Output Add-Ons (§16)

| BIZ-001 Input                     | BIZ-001 States                                         | COM-001 Must Define (Mechanics)                  | Ownership                                        |
| --------------------------------- | ------------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| Extra pages beyond base allowance | §16 "extra pages beyond the base allowance"            | Base page allowance; additional-page pricing     | BIZ-001: output exists. COM-001: page model.     |
| Branding removal                  | §16                                                    | Output add-on pricing and eligibility            | BIZ-001: add-on exists. COM-001: mechanics.      |
| Custom logo placement             | §16                                                    | Output add-on pricing                            | BIZ-001: add-on exists. COM-001: mechanics.      |
| Website embed generation          | §16                                                    | Output add-on pricing                            | BIZ-001: add-on exists. COM-001: mechanics.      |
| Offline interactive packages      | §16; also BIZ-001 §5 "Offline and Self-Hosted Outputs" | Output pricing; package definition               | BIZ-001: output type. COM-001: commercial rules. |
| Self-hosted publication packages  | §16                                                    | Output pricing; hosting-independent output rules | BIZ-001: output type. COM-001: commercial rules. |
| Hosting renewal                   | §16 "hosting renewal"                                  | Renewal pricing mechanics; renewal window        | BIZ-001: output exists. COM-001: renewal rules.  |
| Advanced analytics                | §16                                                    | Add-on eligibility and pricing                   | BIZ-001: add-on exists. COM-001: mechanics.      |

### 2.5 Enterprise Arrangements (§6, §8, §16)

| BIZ-001 Input                                 | BIZ-001 States                                                                                                                                 | COM-001 Must Define (Mechanics)                                                  | Ownership                                                    |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Custom pricing, volume commitments, invoicing | §6 "Large publishers, institutions, and public bodies may negotiate custom pricing, volume commitments, invoicing, and tailored service terms" | Enterprise commercial model; negotiated-contract representation; invoicing flows | BIZ-001: arrangement exists. COM-001: procurement mechanics. |
| Government procurement compatibility          | §8 "procurement-compatible payment (invoicing, purchase orders)"                                                                               | Invoicing, purchase-order, procurement workflows                                 | BIZ-001: segment requirement. COM-001: commercial mechanics. |
| Long-term hosting                             | §8 "long-term publication hosting"                                                                                                             | Hosting commercial terms for enterprise                                          | BIZ-001: requirement. COM-001: hosting mechanics.            |

### 2.6 Revenue Principles (§16)

| BIZ-001 Input                      | BIZ-001 States                                                                           | COM-001 Must Define (Mechanics)                 | Ownership                                   |
| ---------------------------------- | ---------------------------------------------------------------------------------------- | ----------------------------------------------- | ------------------------------------------- |
| Deferred revenue on unused credits | "unused credits represent deferred revenue, not lost revenue"                            | Non-expiry mechanics; accounting boundary       | **Settled** — COM-001 must preserve         |
| Revenue recognition at consumption | "revenue recognition occurs at credit consumption (publication), not at credit purchase" | Consumption events; ledger timing               | **Settled** — COM-001 must respect boundary |
| Detailed rules in COM-001          | "Detailed commercial rules, pricing, and credit mechanics are defined in COM-001"        | (this report defines what COM-001 must contain) | Confirm                                     |

### 2.7 Customer Segments (§8) — Commercial Relevance

| BIZ-001 Segment     | Commercial Implication for COM-001                                 | COM-001 Must Define                                  |
| ------------------- | ------------------------------------------------------------------ | ---------------------------------------------------- |
| Publishing Houses   | Volume credit pricing; recurring workflows; publication libraries  | Volume pricing architecture; subscription allocation |
| Corporate           | Periodic publishing; credit purchases; approval workflows          | Organisation credit allocation; approval gates       |
| NGO / Development   | Low entry cost; pay-per-publication essential                      | Minimum bundle accessibility; pay-per-output path    |
| Government / Public | Procurement-compatible payment; formal approval; long-term hosting | Enterprise invoicing; procurement; hosting terms     |
| Education           | Accessibility; long-term archival; branding                        | Archival commercial terms; institutional pricing     |
| Independent         | Small bundles; pay-per-publication                                 | Minimum bundle; simple purchasing                    |
| Agencies            | Channel, not primary segment                                       | (no special mechanics — confirm non-primary)         |

### 2.8 Market Geography (§11) — Commercial Relevance

| BIZ-001 Input         | BIZ-001 States                                                                                                          | COM-001 Must Define (Mechanics)                                          |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Africa design centre  | §11 "Africa is the design centre"                                                                                       | Country configuration framework; payment-method defaults                 |
| East Africa launch    | §11 "East Africa provides a concentrated launch market"                                                                 | Initial country set; launch commercial configuration                     |
| Progressive expansion | §11 "country-specific payment methods, currencies, tax configurations, and localisation without architectural redesign" | Country commercial configuration model; currency and tax rules framework |

### 2.9 Cost Constraints (§15) — Commercially Relevant

| BIZ-001 Input                 | BIZ-001 States                                                                     | COM-001 Must Respect                                                         |
| ----------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Per-publication margin        | §15 "per-publication margin... must be positive at the lowest credit bundle level" | Base publication pricing must cover variable costs (infrastructure, payment) |
| Payment processing costs      | §15 "transaction fees... variable costs that scale with revenue"                   | Payment strategy must account for fee structures                             |
| Variable cost proportionality | §15 "variable costs should scale proportionally with revenue"                      | Pricing architecture must keep unit economics positive                       |

---

## 3. Ownership Boundary — BIZ-001 vs COM-001

| Concern                                           | Owner                                                  | Boundary                                                                           |
| ------------------------------------------------- | ------------------------------------------------------ | ---------------------------------------------------------------------------------- |
| Product identity, philosophy, principles          | CON-001                                                | Constitutional                                                                     |
| Revenue model / strategy                          | BIZ-001                                                | Business strategy — why and what                                                   |
| Customer segments                                 | BIZ-001                                                | Business strategy                                                                  |
| Market geography                                  | BIZ-001                                                | Business strategy                                                                  |
| Channel architecture                              | BIZ-001                                                | Business strategy                                                                  |
| Commercial mechanics (credits, pricing, payments) | COM-001                                                | Commercial rules — how                                                             |
| Pricing strategy vs pricing architecture          | BIZ-001 owns strategy; COM-001 owns architecture/rules | PA-001 §4.4: "Commercial must not define pricing strategy — COM-001 defines rules" |
| Revenue recognition                               | BIZ-001 sets principle; COM-001 must respect it        | Boundary constraint                                                                |
| Payment provider selection                        | ARC-001 (implementation)                               | COM-001 defines strategy; ARC-001 implements                                       |
| Wallet/Credit/Payment asset models                | DAT-001 (entities); PA-001 (domain); CAP-004 (assets)  | COM-001 defines rules; DAT-001 models entities                                     |
| User personas                                     | USR-001                                                | COM-001 references, does not define                                                |

---

## 4. Settled vs Founder-Decision Items

| Item                               | Status               | Basis                                                                               |
| ---------------------------------- | -------------------- | ----------------------------------------------------------------------------------- |
| Purchased credits do not expire    | **Settled**          | CON-001 PH-003 (no unnecessary commitment); BIZ-001 §16 (deferred revenue not lost) |
| Subscriptions optional             | **Settled**          | CON-001 PH-003; §7.2 Out of Scope "not a mandatory subscription platform"           |
| Revenue recognition at consumption | **Settled**          | BIZ-001 §16                                                                         |
| Pay-per-output primary             | **Settled**          | CON-001 PP-002; BIZ-001 §6                                                          |
| Africa-first design                | **Settled**          | CON-001 PH-006; BIZ-001 §11                                                         |
| Organisations first-class          | **Settled**          | CON-001 PH-007; PP-007                                                              |
| Minimum bundle vs $1 proposition   | **Founder decision** | BIZ-001 states the proposition but not the mechanical distinction                   |
| Inactive-account credit treatment  | **Founder decision** | Not settled by any authoritative document                                           |
| Base page allowance                | **Founder decision** | BIZ-001 references "base allowance" but does not set it                             |
| Hosting duration                   | **Founder decision** | BIZ-001 references hosting lifecycle but not duration                               |
| Add-on pricing model               | **Founder decision** | BIZ-001 lists add-ons but not pricing mechanics                                     |
| Free vs chargeable actions         | **Founder decision** | Guiding rule (legacy CP) exists but no authoritative decision                       |

---

## 5. Summary

BIZ-001 provides a rich, authoritative content foundation for COM-001. Every BIZ-001 commercial input maps to a COM-001 mechanical responsibility. The ownership boundary is clean: **BIZ-001 states what the business does; COM-001 defines how the commercial engine executes it.** Six items are settled constitutionally; six mechanical details require Founder decisions (detailed in COM-WP04-006).

---
