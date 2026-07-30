# BIZ-WP03-004 — Business Model Migration Strategy

**Task:** DOCSFLIP-WP-03-PLAN  
**Date:** 2026-07-30

---

## 1. Migration Overview

| Attribute         | Current           | Target                                           |
| ----------------- | ----------------- | ------------------------------------------------ |
| Version           | 0.1               | 0.2                                              |
| Maturity          | L1 — Skeleton     | L2 — Expanded                                    |
| Structure         | 12 flat sections  | 15 sections in 3 groups (Value/Market/Operating) |
| Domain vocabulary | Pre-PA-001 (v0.1) | PA-001 v0.4 aligned                              |
| CAP traceability  | None              | CAP-001/002/004 referenced                       |

---

## 2. Migration Steps

### Step 1 — Vocabulary Alignment

- Rename "Digital publishing" → "Publications" (per PA-001 §4.3)
- Rename "Organisation management" → "Organisations" (per PA-001 §4.2)
- Remove "Customer support" as a business capability (deferred to ARC-001 per CAP-001 §5)
- Add "Commercial" capability (per PA-001 §4.4)
- Add "Reader Experience" capability (per PA-001 §5.1)
- Add "Identity" capability (per PA-001 §4.1)

### Step 2 — Structural Reorganisation

- Group existing sections into Value Model (1-4), Market Model (5-8), Operating Model (9-15)
- Add Cost Structure (§12)
- Add Key Resources (§10)
- Add Key Partnerships (§11)
- Expand Revenue Streams from Value Capture (§13)

### Step 3 — Traceability Addition

- Add CAP-001 reference to §1 Purpose
- Add PA-001 domain mapping table to §9
- Add CON-001 value proposition reference to §2
- Add USR-001 cross-reference to §5
- Add CAP-004 primary asset reference

### Step 4 — Content Expansion

- Expand Customer Segments with primary/secondary distinction
- Add market geography section (Africa-first per CON-001)
- Decompose Value Capture into revenue streams (credit bundles, organisation subscriptions, enterprise)

---

## 3. Dependencies

| Dependency                  | Status                           |
| --------------------------- | -------------------------------- |
| PA-001 v0.4 authoritative   | ✅ Complete (WP-02R closed)      |
| CAP Framework authoritative | ✅ Complete (PF-007 approved)    |
| CON-001 Founder Approved    | ✅ Complete (WP-01 closed)       |
| USR-001 skeleton            | ✅ Available for cross-reference |

---

## 4. Risks

| Risk                                              | Severity | Mitigation                                                         |
| ------------------------------------------------- | -------- | ------------------------------------------------------------------ |
| Business model scope creep into COM-001 territory | Medium   | Maintain clear separation: BIZ-001 = strategy; COM-001 = mechanics |
| Customer segment detail duplicates USR-001        | Low      | BIZ-001 references USR-001; does not duplicate personas            |

---

## 5. Validation Checkpoints

1. Vocabulary aligned with PA-001 v0.4
2. All 6 PA-001 domains referenced in capabilities
3. CAP-001 traceability present
4. CON-001 value proposition referenced
5. No COM-001 overlap
6. No USR-001 duplication
