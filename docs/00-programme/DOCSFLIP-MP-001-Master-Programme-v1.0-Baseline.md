# DOCSFLIP-MP-001 — Master Programme

**Document ID:** DOCSFLIP-MP-001  
**Title:** Master Programme  
**Version:** 1.2 (WP-01 Closure)  
**Status:** Active  
**Repository Path:** `docs/00-programme/`  
**Authority:** Founder  
**Last Updated:** 2026-07-29

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

The execution sequence governs the order in which work packages are planned. A document's upstream dependencies should be substantially complete before the document enters expansion.

## 7.2 Architectural Dependency Model

Repository influence flows through a directed model in which each document inherits and refines the intent of its upstream parents:

```text
CON-001
    │
    ▼
PA-001
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
- PA-001 translates product intent into architecture domains.
- BIZ-001, COM-001 and USR-001 are peer branches under PA-001.
- JNY-001 derives from USR-001.
- The product chain (USR-001 → JNY-001 → FEA-001 → REQ-001) preserves direct traceability.
- DAT-001 and ARC-001 translate product and commercial intent into technical design.
- IMP-001 is the terminal document, depending on all preceding work.

---

# 8. Repository Document Register

| ID      | Title                    | Area           | Maturity      | Status           | Version | Parent Documents        | Repository Path               |
| ------- | ------------------------ | -------------- | ------------- | ---------------- | ------- | ----------------------- | ----------------------------- |
| MP-001  | Master Programme         | Programme      | L2 (Expanded) | Active           | 1.2     | —                       | `docs/00-programme/`          |
| CON-001 | Product Foundation       | Foundation     | L2 (Expanded) | Founder Approved | 0.2     | MP-001                  | `docs/01-product-foundation/` |
| PA-001  | Product Architecture     | Foundation     | L1 (Skeleton) | Active Draft     | 0.1     | MP-001, CON-001         | `docs/01-product-foundation/` |
| BIZ-001 | Business Model           | Foundation     | L1 (Skeleton) | Active Draft     | 0.1     | MP-001, PA-001          | `docs/01-product-foundation/` |
| COM-001 | Commercial Architecture  | Commercial     | L1 (Skeleton) | Active Draft     | 0.1     | MP-001, PA-001, BIZ-001 | `docs/02-commercial/`         |
| USR-001 | Users & Stakeholders     | Product        | L1 (Skeleton) | Active Draft     | 0.1     | MP-001, PA-001          | `docs/03-product/`            |
| JNY-001 | User Journeys            | Product        | L1 (Skeleton) | Active Draft     | 0.1     | USR-001                 | `docs/03-product/`            |
| FEA-001 | Product Features         | Product        | L1 (Skeleton) | Active Draft     | 0.1     | JNY-001                 | `docs/03-product/`            |
| REQ-001 | Product Requirements     | Product        | L1 (Skeleton) | Active Draft     | 0.1     | FEA-001                 | `docs/03-product/`            |
| DAT-001 | Data Architecture        | Technical      | L0 (Planned)  | Planned          | —       | REQ-001                 | `docs/04-technical/`          |
| ARC-001 | Solution Architecture    | Technical      | L0 (Planned)  | Planned          | —       | DAT-001                 | `docs/04-technical/`          |
| IMP-001 | Implementation Programme | Implementation | L0 (Planned)  | Planned          | —       | ARC-001                 | `docs/05-implementation/`     |

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

Statuses:

- **Proposed** — Idea entered; awaiting Founder assessment.
- **Approved** — Approved for skeleton creation.
- **Deferred** — Postponed with recorded rationale.
- **Rejected** — Declined with rationale.
- **Implemented** — Now a permanent repository document.

---

# 10. Decision Register

All structural decisions affecting the repository, ordered by decision date.

| Ref         | Date       | Decision                                                                                                                                                                                                                                          | Status   |
| ----------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| FD-P1-001   | 2026-07-29 | Adopt Hybrid Dependency Model (execution sequence + architectural dependency)                                                                                                                                                                     | Accepted |
| FD-P1-002   | 2026-07-29 | DOCSFLIP-CONCEPT-001 designated Legacy Product Concept (Source Reference), moved to `docs/legacy/`                                                                                                                                                | Accepted |
| FD-P1-003   | 2026-07-29 | PRC-001, PAY-001, PUB-001 entered into Candidate Register; not added to Repository Document Register                                                                                                                                              | Accepted |
| FD-P1-004   | 2026-07-29 | Initialise operational registers (Candidate, Decision, Deferred, Open Questions, Risk & Assumption) with current programme knowledge                                                                                                              | Accepted |
| FD-WP01-001 | 2026-07-29 | WP-01 Founder Disposition: Accept CON-001 v0.2 with Minor Conditions (3 conditions). Conditions applied: Product Non-goals added, Constitutional Stability statement added, EXP-001 registered as candidate. WP-01 closed. WP-02 authorised next. | Accepted |

---

# 11. Deferred Register

Ideas intentionally postponed so they are not lost.

| Ref | Item                                | Reason for Deferral | Deferred Date |
| --- | ----------------------------------- | ------------------- | ------------- |
| —   | (None recorded at Baseline Closure) | —                   | —             |

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

| Ref    | Type       | Description                                                                                         | Severity | Mitigation                                                         |
| ------ | ---------- | --------------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------ |
| RA-001 | Assumption | Execution sequence is sufficient to govern dependency before expansion stages begin                 | Medium   | Validate at each WP closure                                        |
| RA-002 | Assumption | All skeleton documents will remain stable during Foundation Expansion                               | Low      | Monitor via MP-001 reviews                                         |
| RA-003 | Risk       | Legacy Concept Document may be cited as authoritative by mistake                                    | Low      | Clear markings applied; registered only in Legacy section          |
| RA-004 | Risk       | Candidate documents (PRC-001, PAY-001, PUB-001) may be prematurely referenced in approved documents | Low      | Removed from COM-001 relationships; governed by Candidate Register |
| RA-005 | Assumption | The current repository directory structure (00–05) is sufficient through to engineering preparation | Low      | Review at each phase transition                                    |

---

# 14. Work Package Register

| WP    | Deliverable    | Status  | Founder Disposition          | Conditions | Closure Date | Deliverable  | Maturity Outcome |
| ----- | -------------- | ------- | ---------------------------- | ---------- | ------------ | ------------ | ---------------- |
| WP-01 | Expand CON-001 | Closed  | Accept with Minor Conditions | Satisfied  | 2026-07-29   | CON-001 v0.2 | L2 — Expanded    |
| WP-02 | Expand PA-001  | Planned | —                            | —          | —            | —            | —                |
| WP-03 | Expand BIZ-001 | Planned | —                            | —          | —            | —            | —                |
| WP-04 | Expand COM-001 | Planned | —                            | —          | —            | —            | —                |
| WP-05 | Expand USR-001 | Planned | —                            | —          | —            | —            | —                |
| WP-06 | Expand JNY-001 | Planned | —                            | —          | —            | —            | —                |
| WP-07 | Expand FEA-001 | Planned | —                            | —          | —            | —            | —                |
| WP-08 | Expand REQ-001 | Planned | —                            | —          | —            | —            | —                |

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

Repository Architecture & Skeleton

## Phase 2 — Foundation Expansion

Expand core foundation and commercial documents (WP-01 through WP-08)

## Phase 3 — Technical Definition

Develop DAT-001, ARC-001

## Phase 4 — Engineering Preparation

Develop IMP-001

---

# 16. Repository Dashboard

Track:

- Planned documents: 12 permanent + 1 legacy
- Active work packages: 0
- Completed work packages: 1 (WP-01)
- Foundation Expansion progress: 1 of 8 work packages complete
- Current programme position: WP-01 Closed — WP-02 Next
- CON-001 maturity: L2 — Expanded
- CON-001 status: Founder Approved
- Repository completion: Phase 2 in progress (1/8 WPs)
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

**Current Health Assessment (Baseline Closure):**

| Metric                  | Status                                                  |
| ----------------------- | ------------------------------------------------------- |
| Broken dependencies     | None detected                                           |
| Missing documents       | DAT-001, ARC-001, IMP-001 (Planned L0)                  |
| Duplicate concepts      | Resolved — COM-001 collision eliminated                 |
| Cross-reference quality | Aligned with Hybrid Dependency Model                    |
| Terminology consistency | Corrected — DAT-001 now "Data Architecture" universally |
| Outdated content        | None identified                                         |

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
7. Candidate documents (PRC-001, PAY-001, PUB-001) are governed by the Candidate Register until Founder approval.

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

Phase 2 (Foundation Expansion) is entered when MP-001 records a READY recommendation and WP-01 is activated.
