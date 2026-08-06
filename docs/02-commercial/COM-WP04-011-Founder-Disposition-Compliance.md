# COM-WP04-011 — Founder Disposition Compliance Report

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Disposition — APPROVED WITH MINOR CONDITIONS  
**Authority:** Founder

---

## 1. Founder Disposition

The Founder approved the WP-04 planning package with three minor conditions:

1. **Condition 1:** Confirm that COM-001 defines commercial architecture rather than operational commercial parameters wherever practical.
2. **Condition 2:** Review FD-04 through FD-07 to distinguish architectural rules from configurable commercial values before Loop 2.
3. **Condition 3:** Continue to keep PRC-001, PAY-001 and PUB-001 in the Candidate Register until practical complexity justifies separation.

**Authorisation state:**

- **Loop 1 (Structure Alignment): AUTHORISED** — proceeding requires a separate implementation mandate (expanding COM-001). Not executed during this Analysis-Only phase.
- **Loop 2 (Content Expansion): GATED** on completion of Founder commercial decisions (FD-01..FD-12).

---

## 2. Condition 1 — Architectural vs Operational Parameter Confirmation

### Confirmation: COM-001 defines commercial architecture, not operational parameters.

| Evidence                                                                                                                                                                         | Source                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| "This document defines the commercial operating model of Docsflip. It translates the business model into concrete commercial rules without describing technical implementation." | COM-001 §1 (authoritative)                                                                                        |
| "Specific price points are maintained separately from this document."                                                                                                            | COM-001 §8 (authoritative)                                                                                        |
| "Commercial must not define pricing strategy — COM-001 defines rules."                                                                                                           | PA-001 §4.4 (authoritative)                                                                                       |
| "Detailed commercial rules, pricing, and credit mechanics are defined in COM-001."                                                                                               | BIZ-001 §16 (authoritative)                                                                                       |
| Blueprint sections define **structures, rules, boundaries, and mechanisms** — not specific values                                                                                | COM-WP04-007 §2 (each section lists architectural content, with "subject to Founder decision" markers for values) |

### Architectural vs Configurable Classification Principle

| Layer                               | Owner                                   | Content                                                       | Examples                                                                                                                                  |
| ----------------------------------- | --------------------------------------- | ------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Constitutional**                  | CON-001                                 | Enduring identity, philosophy, principles                     | PH-001..007, PP-001..010                                                                                                                  |
| **Business strategy**               | BIZ-001                                 | Revenue model, segments, geography, channels                  | Value capture, credit bundles, subscriptions                                                                                              |
| **Commercial architecture**         | COM-001                                 | Rules, structures, boundaries, mechanisms, capability mapping | Non-expiry rule, wallet structure, consumption events, approval mechanism, renewal lifecycle, ownership boundaries                        |
| **Configurable operational values** | Maintained separately, Founder-approved | Price points, values, timings, denominations                  | Page counts, hosting durations, renewal windows, grace periods, credit-to-currency values, bundle sizes, tax rates, currency support list |

**Confirmed:** COM-001 must define the **architectural layer** (structures, rules, boundaries, mechanisms). Configurable operational values remain **Founder-approved parameters maintained outside COM-001** — consistent with COM-001 §8, PA-001 §4.4, and the planning blueprint.

---

## 3. Condition 2 — FD-04 through FD-07 Architectural Rule vs Configurable Value Review

### FD-04 — Base Page Allowance

| Dimension                                                                                                                                                 | Classification                                                                                      | Detail                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Base page allowance mechanism** (a defined threshold below which base publication cost covers conversion; above which additional-page charging applies) | **ARCHITECTURAL RULE**                                                                              | The structural mechanism (base allowance + additional-page charging) is a commercial-architecture decision. COM-001 must define the mechanism. |
| Specific base page count (e.g., 50 pages)                                                                                                                 | **CONFIGURABLE VALUE**                                                                              | A price point. Maintained separately, Founder-approved.                                                                                        |
| **Recommendation basis**                                                                                                                                  | Default Option A (fixed base page count) describes the mechanism; the count itself is configurable. |                                                                                                                                                |

### FD-05 — Additional-Page Charging

| Dimension                                                                                                                                       | Classification                                                                  | Detail                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Page-block charging mechanism** (additional pages consumed in defined blocks; credit consumption on block purchase; transparent pre-approval) | **ARCHITECTURAL RULE**                                                          | The block mechanism and its transparency/approval requirements are architectural. COM-001 must define them. |
| Block size and credit cost per block                                                                                                            | **CONFIGURABLE VALUE**                                                          | Price points. Maintained separately.                                                                        |
| **Recommendation basis**                                                                                                                        | Default Option A (block charging) is architectural; block size is configurable. |                                                                                                             |

### FD-06 — Included Hosting Duration

| Dimension                                                                                                                                                           | Classification                                                                    | Detail                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| **Hosting lifecycle structure** (defined initial hosting period included in base output; renewal thereafter as a separate commercial event; non-renewal → archival) | **ARCHITECTURAL RULE**                                                            | The lifecycle structure is architectural. COM-001 must define it. |
| Specific initial duration (e.g., 12 months)                                                                                                                         | **CONFIGURABLE VALUE**                                                            | A commercial parameter. Maintained separately, Founder-approved.  |
| **Recommendation basis**                                                                                                                                            | Default Option A describes the lifecycle structure; the duration is configurable. |                                                                   |

### FD-07 — Hosting Renewal Treatment

| Dimension                                                                                                                                                                      | Classification                                                                                                  | Detail                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **Renewal mechanism** (explicit renewal requiring user action/approval; transparent pricing before action; non-renewal → archival per defined rules; renewal consumes credits) | **ARCHITECTURAL RULE**                                                                                          | The renewal mechanism and its transparency/approval/credit-based properties are architectural. COM-001 must define them. |
| Renewal pricing, renewal window length, grace period                                                                                                                           | **CONFIGURABLE VALUE**                                                                                          | Operational parameters. Maintained separately.                                                                           |
| **Recommendation basis**                                                                                                                                                       | Default Option A (explicit renewal; non-renewal → archival) is architectural; timings/pricing are configurable. |                                                                                                                          |

### Summary Table — FD-04..FD-07

| Ref   | Architectural Rule (COM-001 defines)                                            | Configurable Value (maintained separately) |
| ----- | ------------------------------------------------------------------------------- | ------------------------------------------ |
| FD-04 | Base page allowance mechanism (threshold + additional-page structure)           | Base page count                            |
| FD-05 | Page-block charging mechanism (block model, transparency, approval)             | Block size, credit cost per block          |
| FD-06 | Hosting lifecycle structure (initial period + renewal + archival)               | Initial duration                           |
| FD-07 | Renewal mechanism (explicit, transparent, credit-based; non-renewal → archival) | Renewal pricing, window, grace period      |

**Generalisation:** This architectural-rule vs configurable-value distinction applies to all 12 Founder decisions, not just FD-04..FD-07. It will be applied consistently during Loop 2: each section states the architectural rule in COM-001 and records the configurable values as Founder-approved parameters maintained elsewhere.

---

## 4. Condition 3 — Candidate Register Continuation

**Confirmed:** PRC-001, PAY-001, and PUB-001 remain in the Candidate Register.

| Candidate                          | Status                                                             | Reassessment trigger                                                                    |
| ---------------------------------- | ------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| PRC-001 — Pricing Architecture     | **Remains candidate** — COM-001 absorbs pricing architecture first | After COM-001 closure, if pricing complexity warrants separation                        |
| PAY-001 — Payment Strategy         | **Remains candidate** — COM-001 absorbs payment strategy first     | Phase 3 (Technical Definition), when payment-provider integration complexity is evident |
| PUB-001 — Publication Output Rules | **Remains candidate** — output model is COM-001's centre           | After COM-001 closure, if output-model complexity warrants separation                   |

No candidate files were created. No Candidate Register entries were modified. This preserves the existing COM-WP04-005 recommendation and the Founder's condition.

---

## 5. Implementation Implications for Loop 1 and Loop 2

| Phase                                         | Impact of Conditions                                                                                                                                                                                                                                                                        |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Loop 1 (Structure Alignment)** — Authorised | The 25-section blueprint (COM-WP04-007) already embeds the architectural/operational distinction. Section headers state structures and rules; configurable values are flagged as maintained separately. No structural change required.                                                      |
| **Loop 2 (Content Expansion)** — Gated        | Each section will be written with the architectural-rule / configurable-value distinction applied explicitly. FD-01..FD-12 remain the gate; the Founder's decisions will provide the anchoring for architectural rules, with values (where applicable) recorded as configurable parameters. |
| **Loop 3 (Architectural Integration)**        | Traceability tables will record both the architectural rules (in COM-001) and the location of configurable values (outside COM-001), preserving the FD-12 price-point-governance recommendation.                                                                                            |

---

## 6. Validation

| #   | Check                                                                     | Status |
| --- | ------------------------------------------------------------------------- | ------ |
| 1   | COM-001 was not modified                                                  | ✅     |
| 2   | No candidate document was created                                         | ✅     |
| 3   | No downstream document was modified                                       | ✅     |
| 4   | No commercial policy invented — unresolved items remain Founder decisions | ✅     |
| 5   | Architectural vs operational distinction confirmed with evidence          | ✅     |
| 6   | FD-04..FD-07 architectural-rule/configurable-value review completed       | ✅     |
| 7   | PRC/PAY/PUB candidate continuation confirmed                              | ✅     |
| 8   | Loop 1 authorised but not executed (outside Analysis-Only scope)          | ✅     |
| 9   | Loop 2 gating documented                                                  | ✅     |
| 10  | No WP-04 implementation began                                             | ✅     |

---

## 7. Recommendation

# READY FOR WP-04 FOUNDER COMMERCIAL REVIEW — CONDITIONS SATISFIED

All three Founder conditions are satisfied:

1. **Condition 1 confirmed:** COM-001 defines commercial architecture (rules, structures, boundaries, mechanisms); operational values are Founder-approved parameters maintained separately.
2. **Condition 2 completed:** FD-04 through FD-07 architectural-rule vs configurable-value distinction fully reviewed and documented; applicable generalisation to all 12 decisions recorded.
3. **Condition 3 confirmed:** PRC-001, PAY-001, PUB-001 remain candidates.

**Loop 1 (Structure Alignment) is authorised** and may be executed under a separate implementation mandate when the Founder directs it to begin. **Loop 2 remains gated** on the Founder's commercial decisions (FD-01..FD-12).

---
