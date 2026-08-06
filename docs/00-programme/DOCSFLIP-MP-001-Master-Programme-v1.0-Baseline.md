# DOCSFLIP-MP-001 — Master Programme

**Document ID:** DOCSFLIP-MP-001  
**Title:** Master Programme  
**Version:** 1.8 (Programme Checkpoint Dependency Reconciliation)
**Status:** Active  
**Repository Path:** `docs/00-programme/`  
**Authority:** Founder  
**Last Updated:** 2026-08-06

---

# 1. Purpose

DOCSFLIP-MP-001 is the single authoritative programme management document for the Docsflip documentation repository.

It governs the planning, evolution, execution and monitoring of the repository itself. No other permanent document should duplicate these responsibilities.

---

# 2. Programme Objectives

- Build a complete, coherent and traceable product knowledge repository.
- Define and control the documentation roadmap.
- Govern repository evolution through documented Founder decisions.
- Ensure every document has a defined purpose, dependency and lifecycle.
- Provide a single source of programme truth.

---

# 3. Repository Vision

Create a product knowledge repository that enables anyone joining the project to understand the product from strategy through engineering without relying on historical conversations.

---

# 4. Repository Architecture

```text
docs/
├── 00-programme/
├── 01-product-foundation/
│   └── capability-framework/
├── 02-commercial/
├── 03-product/
├── 04-technical/
├── 05-implementation/
└── legacy/
```

---

# 5. Documentation Development Methodology

The repository is developed using six controlled stages:

1. Repository Architecture
2. Skeleton Development
3. Architecture Review
4. Foundation Expansion
5. Technical Definition
6. Engineering Preparation

A stage must be substantially complete before progressing to the next.

---

# 6. Repository Lifecycle

```text
Idea
 ↓
Candidate
 ↓
Founder Decision
 ↓
Repository Document
 ↓
Skeleton
 ↓
Expansion
 ↓
Review
 ↓
Approved
 ↓
Baseline
 ↓
Maintenance
```

---

# 7. Hybrid Dependency Model

The repository follows a **Hybrid Dependency Model** that distinguishes between the sequence in which documents are developed and the architectural influence between documents.

## 7.1 Execution Sequence

Documents are developed in the following order:

```text
MP-001
↓
CON-001
↓
CAP-000
↓
{ CAP-001, CAP-002, CAP-003, CAP-004, CAP-005 }
↓
PA-001
↓
BIZ-001
↓
COM-001
↓
USR-001
↓
JNY-001
↓
FEA-001
↓
REQ-001
↓
DAT-001
↓
ARC-001
↓
IMP-001
```

The execution sequence governs the order in which work packages are planned. A document's upstream dependencies should be substantially complete before the document enters expansion. The Capability Framework (CAP-000 through CAP-005) is the authoritative capability baseline for PA-001 and all downstream architecture documents.

## 7.2 Architectural Dependency Model

Repository influence flows through a directed model in which each document inherits and refines the intent of its upstream parents:

```text
CON-001
    │
    ▼
CAP-001 (Canonical Capability Model — authoritative)
    │
    ▼
PA-001 (elaborates, does not invent)
 ├──────────────┬──────────────┐
 ▼              ▼              ▼
BIZ-001     COM-001      USR-001
                               │
                               ▼
                           JNY-001
                               ▼
                           FEA-001
                               ▼
                           REQ-001
                               ▼
                           DAT-001
                               ▼
                           ARC-001
                               ▼
                           IMP-001
```

Key observations:

- CON-001 is the root product knowledge document (below MP-001).
- CAP-001 defines the canonical capability model — 6 Level 1 business capabilities. It is authoritative for all downstream architecture.
- PA-001 elaborates capabilities into architecture domains without inventing new ones.
- BIZ-001, COM-001 and USR-001 are architectural peers under PA-001.
- JNY-001 derives from USR-001.
- The product chain (USR-001 → JNY-001 → FEA-001 → REQ-001) preserves direct traceability.
- DAT-001 and ARC-001 translate product and commercial intent into technical design.
- IMP-001 is the terminal document, depending on all preceding work.

**Distinction between dependency types:**

- **Architectural hierarchy** — the directed influence model above. BIZ-001, COM-001 and USR-001 are peers under PA-001. No peer is architecturally upstream or downstream of another.
- **Execution sequence** — the order in which documents are developed (§7.1). This governs work-package planning, not architectural influence.
- **Content dependency** — a document may elaborate content defined in another document without that document being an architectural parent. COM-001 has a content dependency on BIZ-001 (commercial mechanics elaborate the approved business model) but remains an architectural peer of BIZ-001 under PA-001.

---

# 8. Repository Document Register

| ID      | Title                                      | Area           | Maturity      | Status           | Version | Parent Documents                          | Repository Path                                    |
| ------- | ------------------------------------------ | -------------- | ------------- | ---------------- | ------- | ----------------------------------------- | -------------------------------------------------- |
| MP-001  | Master Programme                           | Programme      | L2 (Expanded) | Active           | 1.8     | —                                         | `docs/00-programme/`                               |
| CON-001 | Product Foundation                         | Foundation     | L2 (Expanded) | Founder Approved | 0.2     | MP-001                                    | `docs/01-product-foundation/`                      |
| CAP-000 | Capability Framework                       | Foundation     | L1 (Skeleton) | Active           | 0.1     | MP-001, CON-001                           | `docs/01-product-foundation/capability-framework/` |
| CAP-001 | Canonical Capability Model                 | Foundation     | L1 (Skeleton) | Active           | 0.1     | CAP-000                                   | `docs/01-product-foundation/capability-framework/` |
| CAP-002 | Capability Maps                            | Foundation     | L1 (Skeleton) | Active           | 0.1     | CAP-001                                   | `docs/01-product-foundation/capability-framework/` |
| CAP-003 | Capability Interactions & Bounded Contexts | Foundation     | L1 (Skeleton) | Active           | 0.1     | CAP-001                                   | `docs/01-product-foundation/capability-framework/` |
| CAP-004 | Business Asset Model                       | Foundation     | L1 (Skeleton) | Active           | 0.1     | CAP-001                                   | `docs/01-product-foundation/capability-framework/` |
| CAP-005 | Capability Governance Standard             | Foundation     | L1 (Skeleton) | Active           | 0.1     | CAP-000                                   | `docs/01-product-foundation/capability-framework/` |
| PA-001  | Product Architecture                       | Foundation     | L2 (Expanded) | Active Draft     | 0.4     | MP-001, CON-001, CAP-001                  | `docs/01-product-foundation/`                      |
| BIZ-001 | Business Model                             | Foundation     | L2 (Expanded) | Active Draft     | 0.4     | MP-001, PA-001, CAP-001                   | `docs/01-product-foundation/`                      |
| COM-001 | Commercial Architecture                    | Commercial     | L1 (Skeleton) | Active Draft     | 0.1     | PA-001 (architectural); BIZ-001 (content) | `docs/02-commercial/`                              |
| USR-001 | Users & Stakeholders                       | Product        | L1 (Skeleton) | Active Draft     | 0.1     | MP-001, PA-001                            | `docs/03-product/`                                 |
| JNY-001 | User Journeys                              | Product        | L1 (Skeleton) | Active Draft     | 0.1     | USR-001                                   | `docs/03-product/`                                 |
| FEA-001 | Product Features                           | Product        | L1 (Skeleton) | Active Draft     | 0.1     | JNY-001                                   | `docs/03-product/`                                 |
| REQ-001 | Product Requirements                       | Product        | L1 (Skeleton) | Active Draft     | 0.1     | FEA-001                                   | `docs/03-product/`                                 |
| DAT-001 | Data Architecture                          | Technical      | L0 (Planned)  | Planned          | —       | REQ-001                                   | `docs/04-technical/`                               |
| ARC-001 | Solution Architecture                      | Technical      | L0 (Planned)  | Planned          | —       | DAT-001                                   | `docs/04-technical/`                               |
| IMP-001 | Implementation Programme                   | Implementation | L0 (Planned)  | Planned          | —       | ARC-001                                   | `docs/05-implementation/`                          |

## 8.1 Legacy Document Register

| ID          | Title                                     | Location       | Status                     |
| ----------- | ----------------------------------------- | -------------- | -------------------------- |
| CONCEPT-001 | Legacy Product Concept (Source Reference) | `docs/legacy/` | Legacy — Non-authoritative |

---

# 9. Candidate Register

Documents proposed but not yet approved for repository entry.

| ID      | Title                    | Proposed Area | Status   | Notes                                                                                                                                                                                                     |
| ------- | ------------------------ | ------------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| PRC-001 | Pricing Architecture     | Commercial    | Proposed | Future sub-document of COM-001. Not yet approved.                                                                                                                                                         |
| PAY-001 | Payment Strategy         | Commercial    | Proposed | Future sub-document of COM-001. Not yet approved.                                                                                                                                                         |
| PUB-001 | Publication Output Rules | Commercial    | Proposed | Future sub-document of COM-001. Not yet approved.                                                                                                                                                         |
| EXP-001 | Product Experience       | Product       | Proposed | Candidate for experience philosophy, interaction principles, emotional goals, accessibility philosophy and design-language direction. Must not be created without Founder approval and demonstrated need. |

---

# 10. Decision Register

All structural decisions affecting the repository, ordered by decision date.

| Ref          | Date       | Decision                                                                                                                                                                                                                                                                                                                                                                                                              | Status   |
| ------------ | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| FD-P1-001    | 2026-07-29 | Adopt Hybrid Dependency Model (execution sequence + architectural dependency)                                                                                                                                                                                                                                                                                                                                         | Accepted |
| FD-P1-002    | 2026-07-29 | DOCSFLIP-CONCEPT-001 designated Legacy Product Concept (Source Reference), moved to `docs/legacy/`                                                                                                                                                                                                                                                                                                                    | Accepted |
| FD-P1-003    | 2026-07-29 | PRC-001, PAY-001, PUB-001 entered into Candidate Register; not added to Repository Document Register                                                                                                                                                                                                                                                                                                                  | Accepted |
| FD-P1-004    | 2026-07-29 | Initialise operational registers (Candidate, Decision, Deferred, Open Questions, Risk & Assumption) with current programme knowledge                                                                                                                                                                                                                                                                                  | Accepted |
| FD-WP01-001  | 2026-07-29 | WP-01 Founder Disposition: Accept CON-001 v0.2 with Minor Conditions (3 conditions). Conditions applied: Product Non-goals added, Constitutional Stability statement added, EXP-001 registered as candidate. WP-01 closed. WP-02 authorised next.                                                                                                                                                                     | Accepted |
| FD-PF-001    | 2026-07-29 | Capability Framework (CAP-000 through CAP-005) approved in principle. Phase A analysis complete. Phase B integration authorised.                                                                                                                                                                                                                                                                                      | Accepted |
| FD-PF-002    | 2026-07-29 | Capability Framework integrated into repository. CAP documents relocated to `capability-framework/`. MP-001 dependency chain, document register and architectural model updated. PA-001, CON-001, COM-001, USR-001 cross-references added.                                                                                                                                                                            | Accepted |
| FD-VG-001    | 2026-07-29 | PF-007 Capability Framework Validation Gate APPROVED. CAP-000 through CAP-005 are the authoritative capability baseline for PA-001 and all downstream architecture documents.                                                                                                                                                                                                                                         | Accepted |
| FD-WP02-001  | 2026-07-29 | WP-02 — Expand PA-001 CLOSED — SUPERSEDED by WP-02R. WP-02 scope assumed existing PA-001 domain structure was valid. Superseded by Capability Framework integration and PA-001 structural refactoring plan. Existing WP-02 artefacts preserved.                                                                                                                                                                       | Accepted |
| FD-WP02R-001 | 2026-07-29 | WP-02R — Capability-Aligned Product Architecture Refactoring CREATED. Three controlled loops: Loop 1 (Structural Refactoring — Authorised), Loop 2 (Domain Content — Planned), Loop 3 (Relationships and Traceability — Planned).                                                                                                                                                                                     | Accepted |
| FD-WP02R-002 | 2026-07-29 | WP-02R Loop 1 (Structural Refactoring) AUTHORISED. Execute the approved migrations from PA-RP-002 and PA-RP-004 Phase 1. Do not proceed to Loop 2 or Loop 3 without further Founder approval.                                                                                                                                                                                                                         | Accepted |
| FD-WP02R-003 | 2026-07-29 | WP-02R Loop 2 (Domain Content Expansion) APPROVED and AUTHORISED. PA-001 promoted to L2 — Expanded.                                                                                                                                                                                                                                                                                                                   | Accepted |
| FD-WP02R-004 | 2026-07-29 | WP-02R Loop 3 (Relationships and Traceability) APPROVED and AUTHORISED.                                                                                                                                                                                                                                                                                                                                               | Accepted |
| FD-WP02R-005 | 2026-07-30 | WP-02R FORMALLY CLOSED. All three loops complete. PA-001 v0.4, L2 Expanded, accepted as authoritative Product Architecture baseline. WP-03 authorised next.                                                                                                                                                                                                                                                           | Accepted |
| FD-WP03-001  | 2026-07-30 | WP-03 FORMALLY CLOSED. All three loops (Structure, Content, Integration) complete. BIZ-001 v0.4, L2 Expanded, accepted as authoritative Business Model baseline. WP-04 authorised next.                                                                                                                                                                                                                               | Accepted |
| FD-CHKPT-001 | 2026-08-06 | Programme Checkpoint 001 APPROVED. CON-001, PA-001 and BIZ-001 accepted as stable baseline. Dependency reconciliation authorised: BIZ-001 §19 corrected to peer-branch model; COM-001 classified as content-dependent on BIZ-001 (architectural parent PA-001); MP-001 §7.2 distinction added between architectural hierarchy, execution sequence and content dependency. WP-04 Planning authorised after validation. | Accepted |

---

# 11. Deferred Register

Ideas intentionally postponed so they are not lost.

| Ref    | Item                                                                                                | Reason for Deferral                                                                                                  | Deferred Date |
| ------ | --------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ------------- |
| DF-001 | CAP-000, CAP-001, CAP-005 downstream-list maintenance (add BIZ-001 to downstream document lists)    | Low-priority traceability completeness. Add during a future Capability Framework maintenance pass, not before WP-04. | 2026-08-06    |
| DF-002 | FEA-001 domain realignment to PA-001's 6 domains (remove "Administration", add "Reader Experience") | To be addressed during WP-07 Planning. Does not block WP-04, WP-05 or WP-06.                                         | 2026-08-06    |

---

# 12. Open Questions Register

Unresolved architectural and product questions awaiting Founder direction.

| Ref    | Question                                                                      | Context                                           | Raised Date |
| ------ | ----------------------------------------------------------------------------- | ------------------------------------------------- | ----------- |
| OQ-001 | DAT-001 document file name and location to be confirmed when skeleton created | DAT-001 is L0 (Planned); currently no file exists | 2026-07-29  |
| OQ-002 | ARC-001 document file name and location to be confirmed when skeleton created | ARC-001 is L0 (Planned); currently no file exists | 2026-07-29  |
| OQ-003 | IMP-001 document file name and location to be confirmed when skeleton created | IMP-001 is L0 (Planned); currently no file exists | 2026-07-29  |

**Disposed Questions (WP-01):**

| Ref         | Question                                                                                        | Disposition                                                                                                                                                 | Disposed Date |
| ----------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| OQ-WP01-001 | Should "Product Experience Vision" be restored as a distinct section?                           | **Closed.** Do not add Product Experience Vision to CON-001. EXP-001 registered as Candidate for future experience philosophy. Found in Candidate Register. | 2026-07-29    |
| OQ-WP01-002 | Should Product Pillars be retained as a separate construct or absorbed into Product Principles? | **Closed.** Product Pillars remain absorbed into Product Philosophy and Product Principles. No separate Pillars construct required at this time.            | 2026-07-29    |
| OQ-WP01-003 | Should Target Customers retain a customer-segment list or be owned entirely by BIZ-001?         | **Closed.** Product-level user categories remain in CON-001 (§8). Detailed customer segmentation remains with BIZ-001 and USR-001.                          | 2026-07-29    |

---

# 13. Risk & Assumption Register

Architectural assumptions, dependencies and known risks affecting repository evolution.

| Ref    | Type       | Description                                                                                         | Severity | Mitigation                                                                                      |
| ------ | ---------- | --------------------------------------------------------------------------------------------------- | -------- | ----------------------------------------------------------------------------------------------- |
| RA-001 | Assumption | Execution sequence is sufficient to govern dependency before expansion stages begin                 | Medium   | Validate at each WP closure                                                                     |
| RA-002 | Assumption | All skeleton documents will remain stable during Foundation Expansion                               | Low      | Monitor via MP-001 reviews                                                                      |
| RA-003 | Risk       | Legacy Concept Document may be cited as authoritative by mistake                                    | Low      | Clear markings applied; registered only in Legacy section                                       |
| RA-004 | Risk       | Candidate documents may be prematurely referenced in approved documents                             | Low      | All candidate documents governed by Candidate Register; removed from active document references |
| RA-005 | Assumption | The current repository directory structure (00–05) is sufficient through to engineering preparation | Low      | Review at each phase transition                                                                 |

---

# 14. Work Package Register

| WP     | Deliverable                                         | Status              | Founder Disposition  | Conditions | Closure Date | Deliverable  | Maturity Outcome        |
| ------ | --------------------------------------------------- | ------------------- | -------------------- | ---------- | ------------ | ------------ | ----------------------- |
| WP-01  | Expand CON-001                                      | Closed              | Accept with Minor    | Satisfied  | 2026-07-29   | CON-001 v0.2 | L2 — Expanded           |
| WP-02  | Expand PA-001                                       | Closed — Superseded | Superseded by WP-02R | —          | 2026-07-29   | —            | Superseded              |
| WP-02R | Capability-Aligned Product Architecture Refactoring | Closed              | Founder Authorised   | Satisfied  | 2026-07-30   | PA-001 v0.4  | L2 — Expanded (3 loops) |
| WP-03  | Expand BIZ-001                                      | Closed              | Founder Authorised   | Satisfied  | 2026-07-30   | BIZ-001 v0.4 | L2 — Expanded (3 loops) |
| WP-04  | Expand COM-001                                      | Planned             | —                    | —          | —            | —            | —                       |
| WP-05  | Expand USR-001                                      | Planned             | —                    | —          | —            | —            | —                       |
| WP-06  | Expand JNY-001                                      | Planned             | —                    | —          | —            | —            | —                       |
| WP-07  | Expand FEA-001                                      | Planned             | —                    | —          | —            | —            | —                       |
| WP-08  | Expand REQ-001                                      | Planned             | —                    | —          | —            | —            | —                       |

Each work package follows:

- Review
- Gap Analysis
- Expansion
- Validation
- Founder Review
- Approval
- MP-001 Update
- Closure

---

# 15. Programme Roadmap

## Phase 1 — Programme Design

Repository Architecture & Skeleton. Complete.

## Phase 2 — Foundation Expansion

Expand core foundation and commercial documents (WP-01 through WP-08). CON-001, PA-001, BIZ-001 complete. COM-001 next.

## Phase 3 — Technical Definition

Develop DAT-001, ARC-001

## Phase 4 — Engineering Preparation

Develop IMP-001

---

# 16. Repository Dashboard

Track:

- Planned documents: 18 permanent + 1 legacy
- Active work packages: 0
- Completed work packages: 4 (WP-01, WP-02, WP-02R, WP-03)
- Foundation Expansion progress: CON-001, PA-001, BIZ-001 complete; COM-001 next
- Current programme position: WP-03 Closed — WP-04 Next
- CON-001 maturity: L2 — Expanded (Founder Approved)
- PA-001 maturity: L2 — Expanded (v0.4, authoritative baseline)
- BIZ-001 maturity: L2 — Expanded (v0.4, authoritative baseline)
- Capability Framework: Authoritative baseline
- Repository completion: Phase 2 in progress (3/8 foundation documents complete)
- Candidate proposals: 4 (PRC-001, PAY-001, PUB-001, EXP-001)

---

# 17. Repository Health

Monitor:

- Broken dependencies
- Missing documents
- Duplicate concepts
- Cross-reference quality
- Terminology consistency
- Outdated content

**Current Health Assessment (WP-03 Closure):**

| Metric                  | Status                                               |
| ----------------------- | ---------------------------------------------------- |
| Broken dependencies     | None detected                                        |
| Missing documents       | DAT-001, ARC-001, IMP-001 (Planned L0)               |
| Duplicate concepts      | Resolved — COM-001 collision eliminated              |
| Cross-reference quality | Aligned with Hybrid Dependency Model + CAP Framework |
| Terminology consistency | Consistent across all documents                      |
| Outdated content        | None. CON-001, PA-001, BIZ-001 complete.             |

---

# 18. Repository Maturity Model

| Level | Meaning  |
| ----- | -------- |
| L0    | Planned  |
| L1    | Skeleton |
| L2    | Expanded |
| L3    | Reviewed |
| L4    | Approved |
| L5    | Baseline |

---

# 19. Operating Rules

1. MP-001 is the single programme control document.
2. No permanent document is created without passing through the Candidate Register and Founder approval.
3. Every structural repository decision must be recorded in the Decision Register.
4. Every completed work package must update MP-001.
5. Every conversation that changes the repository ends with an MP-001 update.
6. Legacy documents must never override approved repository documents.
7. All candidate documents are governed by the Candidate Register until Founder approval. Candidate identifiers must not be treated as permanent repository documents, added to the active dependency model, or created as files before approval.
8. The Capability Framework (CAP-000 through CAP-005) defines the canonical business capabilities. No downstream document may redefine the capability model without Founder constitutional amendment. CAP-000 through CAP-005 are authoritative for PA-001 and all downstream architecture documents.

---

# 20. Programme Exit Criteria

Phase 1 (Programme Design) is complete when:

- Core foundation documents are approved.
- Repository architecture is stable.
- Traceability is established.
- Technical definition can begin without structural redesign.
- Hybrid Dependency Model is accepted.
- Operational registers are initialised.
- Baseline Closure is confirmed.

**Phase 1 Status: COMPLETE — Baseline Closure achieved 2026-07-29.**

Phase 2 is active. WP-01, WP-02R, and WP-03 are closed. CON-001, PA-001, and BIZ-001 are complete and authoritative. WP-04 (Expand COM-001) is the next authorised work package.
