# COM-WP04-008 — Implementation and Migration Strategy

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised

---

## 1. Purpose

This report recommends the implementation approach for expanding COM-001 from L1 Skeleton to L2 Expanded. It assesses the established three-loop pattern and proposes the migration strategy from the current 14-section skeleton to the 25-section target structure.

---

## 2. Implementation Approach Assessment

### 2.1 Established Three-Loop Pattern

The repository has successfully used the three-loop pattern twice:

| WP              | Loop 1                 | Loop 2                   | Loop 3                         |
| --------------- | ---------------------- | ------------------------ | ------------------------------ |
| WP-02R (PA-001) | Structural Refactoring | Domain Content Expansion | Relationships and Traceability |
| WP-03 (BIZ-001) | Structure Alignment    | Content Expansion        | Architectural Integration      |

Both closed with all validation PASS.

### 2.2 COM-001 Complexity Assessment

| Complexity Signal             | COM-001                                                               |
| ----------------------------- | --------------------------------------------------------------------- |
| Target sections               | 25                                                                    |
| Source sections               | 14                                                                    |
| Content units (estimate)      | ~138                                                                  |
| Capability alignment required | 5 sub-capabilities (Wallet, Credits, Payments, Entitlements, Outputs) |
| Business-model inputs         | 9 BIZ-001 content areas                                               |
| Constitutional constraints    | 9 settled + 12 Founder decisions                                      |
| Downstream consumers          | 8 documents                                                           |
| Existing content continuity   | 8 components preserved                                                |

**Assessment:** Comparable to BIZ-001's expansion complexity (20 sections, 3 groups). The three-loop pattern is appropriate. **A different number of loops is NOT recommended** — the established pattern is proportionate and validated.

---

## 3. Recommended Implementation Approach — Three Loops

### Loop 1 — Structure Alignment

| Element                                       | Detail                                                                                                    |
| --------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **Goal**                                      | Restructure COM-001 from 14 flat sections into the 9-part / 25-section target framework (COM-WP04-007 §2) |
| **Preserves**                                 | All 14 existing skeleton sections mapped into target sections (preservation map in COM-WP04-007 §4)       |
| **Constitutional groundings**                 | Add explicit CON-001 PH/PP citations to the Commercial Philosophy section                                 |
| **Capability alignment**                      | Add CAP-001/002/004 and PA-001 §4.4 references into a structure-alignment matrix                          |
| **Boundary statement**                        | Add "COM-001 owns / does not own" section (mirrors BIZ-001 §2)                                            |
| **Dependency interpretation**                 | Record architectural peer status (BIZ-001, COM-001, USR-001 under PA-001) + content dependency on BIZ-001 |
| **Can proceed with settled constraints only** | Yes — Loop 1 requires no Founder decisions                                                                |
| **Validation gates**                          | Structure completeness; source preservation; capability alignment; terminal checks                        |

### Loop 2 — Commercial Content Expansion

| Element                        | Detail                                                                                                                                                                                        |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Goal**                       | Expand all 25 sections with full commercial content                                                                                                                                           |
| **Prerequisite**               | **Founder decisions FD-01 through FD-12 (COM-WP04-006)**                                                                                                                                      |
| **Settled content**            | Write sections fully grounded in settled constraints (non-expiry, optional subscriptions, output-based value, transparency, Africa-first, organisations-first)                                |
| **Decision-dependent content** | Write each section according to the Founder's decision for FD-01 through FD-12                                                                                                                |
| **Content volume**             | ~138 content units across 25 sections                                                                                                                                                         |
| **Validation gates**           | Constitutional traceability (each section cites PH/PP); capability traceability (each component maps to CAP-001/002/004); business-input traceability (BIZ-001 §6/§8/§16); no invented policy |

### Loop 3 — Architectural Integration

| Element                    | Detail                                                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Goal**                   | Complete traceability, downstream consumers, governance, exceptions, and integration                         |
| **Traceability**           | Full tables: CAP-001/002/004 → PA-001 §4.4 → BIZ-001 inputs → CON-001 PH/PP → downstream consumers           |
| **Downstream consumers**   | Documented for USR-001, JNY-001, FEA-001, REQ-001, DAT-001, ARC-001, IMP-001                                 |
| **Governance**             | Commercial governance principles, exceptions framework, price-point governance                               |
| **Foundational decisions** | Codify all settled + Founder-approved commercial decisions                                                   |
| **Validation gates**       | No circular dependency; no new L1 capabilities; ownership boundaries intact; MP-001 metadata remains aligned |

---

## 4. Migration Strategy — Skeleton to Target

### 4.1 One-Step Structural Migration (Loop 1)

The current 14 sections map directly into the target 25 sections. Because the skeleton is small (168 lines) and every section is preserved (COM-WP04-007 §4), a **single structural rewrite in Loop 1** is appropriate — not a phased migration.

| Migration Step      | Action                                                             |
| ------------------- | ------------------------------------------------------------------ |
| Step 1              | Read current COM-001 v0.1 complete                                 |
| Step 2              | Create target 25-section skeleton with all existing content placed |
| Step 3              | Add new section headers with placeholders (structure-first)        |
| Step 4              | Add constitutional citations to §3                                 |
| Step 5              | Add ownership-boundary §2 and structure-overview §2                |
| Step 6              | Validate structure against COM-WP04-007 §2                         |
| **Loop 1 Complete** | COM-001 v0.2, L1 — restructured skeleton                           |

### 4.2 Content Expansion (Loop 2)

| Migration Step      | Action                                      |
| ------------------- | ------------------------------------------- |
| Step 1              | Apply all 12 Founder decisions              |
| Step 2              | Expand Credit & Wallet (Part 2)             |
| Step 3              | Expand Publication Output (Part 3)          |
| Step 4              | Expand Pricing & Entitlements (Part 4)      |
| Step 5              | Expand Payments & Market (Part 5)           |
| Step 6              | Expand Organisation & Enterprise (Part 6)   |
| Step 7              | Expand Hosting & Account Lifecycle (Part 7) |
| Step 8              | Expand Governance & Exceptions (Part 8)     |
| **Loop 2 Complete** | COM-001 v0.3, L2 — content expanded         |

### 4.3 Architectural Integration (Loop 3)

| Migration Step      | Action                                                         |
| ------------------- | -------------------------------------------------------------- |
| Step 1              | Build full traceability tables                                 |
| Step 2              | Document downstream consumers                                  |
| Step 3              | Codify Foundational Decisions                                  |
| Step 4              | Validate no new L1 capabilities                                |
| Step 5              | Validate no circular dependencies                              |
| Step 6              | Confirm MP-001 register alignment (version, parents, maturity) |
| **Loop 3 Complete** | COM-001 v0.4, L2 — fully integrated                            |

---

## 5. Version and Maturity Progression

| Phase           | Version | Maturity                   |
| --------------- | ------- | -------------------------- |
| Start (current) | 0.1     | L1 — Skeleton              |
| Loop 1 complete | 0.2     | L1 (restructured)          |
| Loop 2 complete | 0.3     | L2 — Expanded              |
| Loop 3 complete | 0.4     | L2 — Expanded (integrated) |

This mirrors the established version progression of PA-001 (v0.1→v0.4) and BIZ-001 (v0.1→v0.4).

---

## 6. Execution Ordering Recommendation

| Phase                                | Condition                                                                                     |
| ------------------------------------ | --------------------------------------------------------------------------------------------- |
| Loop 1 — Structure Alignment         | Can proceed immediately after Founder authorisation; **requires no new commercial decisions** |
| **Founder Commercial Review (Gate)** | Loop 1 complete; Founder reviews structure; Founder provides decisions FD-01 through FD-12    |
| Loop 2 — Content Expansion           | Requires all 12 Founder decisions                                                             |
| **Founder Review (Gate)**            | Loop 2 complete                                                                               |
| Loop 3 — Architectural Integration   | No additional decisions required                                                              |
| **Founder Approval + Closure**       | Loop 3 complete; MP-001 updated                                                               |

---

## 7. Open Risks and Mitigations

| Risk                                        | Mitigation                                                                                                                    |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Founder decisions FD-01..FD-12 delay Loop 2 | Loop 1 gate is the natural decision point; decisions can be made progressively (tranche 1 before Loop 2, tranches 2-3 during) |
| Scope creep beyond commercial mechanics     | Enforce ownership boundary from COM-WP04-001 §7; reject non-commercial content                                                |
| Unintended new L1 capability                | CAP-005 governance check at each loop                                                                                         |
| Price-point invention                       | Price points remain Founder-approved values outside COM-001 (FD-12 recommendation)                                            |
| Provider selection                          | Deferred to ARC-001 (COM-001 §9 boundary maintained)                                                                          |
| Downstream misalignment                     | Downstream impact assessment (COM-WP04-009) pre-registered; each downstream document aligns during its own WP                 |

---

## 8. Recommendation

**Use the established three-loop pattern:**

1. **Loop 1 — Structure Alignment** (v0.1 → v0.2)
2. **Loop 2 — Commercial Content Expansion** (v0.2 → v0.3)
3. **Loop 3 — Architectural Integration** (v0.3 → v0.4)

**A different number of loops is not supported by evidence.** COM-001's complexity is comparable to BIZ-001 (20 sections, 3 groups), which was successfully completed in three loops. The single structural migration is appropriate because the skeleton is small and fully preservable.

The critical path is **Loop 1 → Founder Commercial Review (decisions FD-01..FD-12) → Loop 2 → Loop 3 → Closure**.

---
