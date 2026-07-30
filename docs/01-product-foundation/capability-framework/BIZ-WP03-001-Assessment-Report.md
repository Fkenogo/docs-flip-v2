# BIZ-WP03-001 — WP-03 Business Model Assessment Report

**Task:** DOCSFLIP-WP-03-PLAN  
**Date:** 2026-07-30  
**Status:** Analytical — no BIZ-001 changes made

---

## 1. Current State

BIZ-001 v0.1 is an L1 Skeleton with 12 sections defining how Docsflip creates, delivers, and captures value. It correctly separates business strategy from commercial mechanics (delegated to COM-001). However, it was written before the Capability Framework and PA-001 refactoring, and its architecture vocabulary is outdated.

---

## 2. Assessment Against Authoritative Documents

### 2.1 CON-001 Alignment

| CON-001 Element    | BIZ-001 Coverage                                                     | Assessment                                                                  |
| ------------------ | -------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Product Identity   | Implicit in business model summary                                   | Adequate for skeleton — needs explicit identity reference                   |
| Product Philosophy | Value Creation aligns with PH-001 (Publishing Outcomes Define Value) | Adequate                                                                    |
| Target Users       | Customer Segments lists 6 segments                                   | Needs alignment with CON-001 user categories                                |
| Product Scope      | "Digital publishing" captures scope                                  | Needs PA-001 domain traceability                                            |
| Value Proposition  | Implicit in value creation/delivery/capture                          | Missing explicit VP reference                                               |
| Product Non-goals  | None                                                                 | Missing — business model should reference what the business does not pursue |

### 2.2 Capability Framework Alignment

| CAP Document | BIZ-001 Coverage | Assessment                                                     |
| ------------ | ---------------- | -------------------------------------------------------------- |
| CAP-001      | No reference     | Missing — capability model should anchor business capabilities |
| CAP-002      | No reference     | Missing                                                        |
| CAP-004      | No reference     | Missing — publication as primary business asset not referenced |

### 2.3 PA-001 Alignment

| Issue                          | Detail                                                                                                                        |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| Domain vocabulary outdated     | §9 "Key Capabilities" uses "Digital publishing" instead of PA-001's "Publications"; "Customer support" is not a PA-001 domain |
| Missing domain traceability    | §9 lists 6 capabilities — none map explicitly to PA-001's 6 domains                                                           |
| Organization → Organisations   | §9 "Organisation management" should map to PA-001 Organisations domain                                                        |
| No Reader Experience reference | Business model does not acknowledge reader value delivery                                                                     |
| No Analytics reference         | §9 lists "Analytics" but does not tie to PA-001's Analytics domain                                                            |

---

## 3. Structural Weaknesses

| Weakness                             | Detail                                                                               |
| ------------------------------------ | ------------------------------------------------------------------------------------ |
| Flat structure                       | 12 sections, no grouping (Value Model / Market Model / Operating Model)              |
| No value stream mapping              | How value flows from publishing through commercial to reader not described           |
| No cost structure                    | What it costs to deliver the business model is absent                                |
| No key resources                     | Human, technological, and partner resources not identified                           |
| No key partnerships                  | Payment providers, technology partners not mentioned                                 |
| No revenue model detail              | "Revenue generated when customers publish" is stated but not decomposed              |
| No business model canvas integration | Sections align with Business Model Canvas concepts but are not explicitly structured |
| Customer segments are flat           | No distinction between primary/secondary/tertiary segments                           |
| No market sizing                     | Africa-wide ambition stated in CON-001 but not reflected in BIZ-001                  |
| No competitive position              | Strategic differentiators exist but no competitive landscape                         |

---

## 4. Duplicated Concepts

| Concept              | BIZ-001                 | Other Document | Resolution                                                         |
| -------------------- | ----------------------- | -------------- | ------------------------------------------------------------------ |
| Commercial mechanics | §5 delegates to COM-001 | COM-001        | ✅ Correct — maintain separation                                   |
| User definitions     | Customer Segments §6    | USR-001        | ⚠️ BIZ-001 should reference USR-001, not duplicate user categories |

---

## 5. Incorrect Ownership

| Item                             | Currently In | Should Be In                                                      | Reason                                        |
| -------------------------------- | ------------ | ----------------------------------------------------------------- | --------------------------------------------- |
| Customer segments detail         | BIZ-001 §6   | BIZ-001 owns business segmentation; USR-001 expands user profiles | ✅ Correct, but needs USR-001 cross-reference |
| "Customer support" as capability | BIZ-001 §9   | Not a PA-001 domain; operational concern → ARC-001                | ⚠️ Remove from business capabilities          |

---

## 6. Missing Traceability

| Missing From         | Missing To                          | Impact                                            |
| -------------------- | ----------------------------------- | ------------------------------------------------- |
| BIZ-001 purpose      | CON-001 Vision, Mission, Philosophy | Low — implicit but should be explicit             |
| BIZ-001 capabilities | PA-001 domains                      | Medium — downstream traceability broken           |
| BIZ-001 capabilities | CAP-001 capabilities                | Medium — constitutional traceability missing      |
| BIZ-001 assets       | CAP-004 business assets             | Low — publication as primary asset not referenced |

---

## 7. Conflicts with PA-001

| Conflict                               | Detail                                                                                                      |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| "Digital publishing" vs "Publications" | PA-001 defines Publications as the domain owning creation, management, distribution of digital publications |
| "Customer support" as capability       | PA-001 deferred Administration to ARC-001; not a business capability                                        |
| No Organisations domain reference      | BIZ-001 should map value delivery to Organisations (workspace, team publishing)                             |
| No Commercial domain reference         | BIZ-001 references COM-001 for rules but not PA-001 Commercial domain for capability                        |
| No Reader Experience reference         | PA-001 defines Reader Experience as a supporting domain; BIZ-001 should acknowledge reader value            |

---

## 8. Maturity Assessment

BIZ-001 is at **L1 — Skeleton.** It has a coherent structure and appropriate conceptual boundaries (separating business strategy from commercial mechanics). However, it lacks Capability Framework traceability, PA-001 domain alignment, and several standard business model components (cost structure, key resources, partnerships, revenue model decomposition).

**Ready for expansion with structural modernisation.**
