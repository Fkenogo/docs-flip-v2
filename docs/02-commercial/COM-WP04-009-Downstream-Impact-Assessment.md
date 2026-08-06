# COM-WP04-009 — Downstream Impact Assessment

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised

---

## 1. Purpose

This report assesses the impact of the planned COM-001 expansion on all downstream documents. Each document is classified as: **no change**, **metadata alignment**, **minor alignment**, or **major redesign**.

**No downstream document was modified by this assessment.**

---

## 2. Downstream Impact Summary

| Document      | Classification         | Detail                                                                                                                                                                                                                                                                                                   |
| ------------- | ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| USR-001       | **Metadata alignment** | COM-001 expansion defines commercial roles (payer, administrator, organisation admin). USR-001 may need to reference commercial roles more precisely during its own WP-05. No structural impact.                                                                                                         |
| JNY-001       | **Minor alignment**    | JNY-001 (skeleton) includes J6 "Acquire Publishing Capacity" and J5 "Preview Publication". COM-001's cost-preview and approval mechanics will inform journey detail during WP-06. No journey list change required.                                                                                       |
| FEA-001       | **Minor alignment**    | FEA-001 has feature domain "D. Commercial" (Wallet, Credits, Transactions, Purchase History). COM-001's expanded commercial surface (entitlements, add-ons, renewal, enterprise) will require FEA-001's Commercial domain expansion during WP-07. Domain realignment (DF-002) already deferred to WP-07. |
| REQ-001       | **Minor alignment**    | REQ-001's initial requirement catalogue has FR-007 "manage publishing credits". COM-001 expansion will supply the commercial rules that REQ-001 must translate into requirements during WP-08.                                                                                                           |
| DAT-001       | **Minor alignment**    | DAT-001 (L0, Planned) will need to model Wallet, Credit, Payment, Transaction, Entitlement entities per CAP-004 and PA-001 §4.4. COM-001's commercial rules will inform entity behaviour. No change to DAT-001 yet (Phase 3).                                                                            |
| ARC-001       | **Minor alignment**    | ARC-001 (L0, Planned) implements the Commercial domain (payment gateway, ledger, wallet). COM-001 defines commercial strategy; ARC-001 implements. COM-001 must maintain the "COM-001 defines, ARC-001 implements" boundary. No change now.                                                              |
| IMP-001       | **No change**          | IMP-001 (L0, Planned) is terminal. COM-001 expansion adds commercial-definition content but no new implementation programme requirements at this stage.                                                                                                                                                  |
| MP-001        | **Metadata alignment** | MP-001 Document Register must be updated at COM-001 expansion closure: version 0.1→0.4, maturity L1→L2, parents remain `PA-001 (architectural); BIZ-001 (content)`. This is a closure-time update, not a planning-time change.                                                                           |
| BIZ-001       | **No change**          | BIZ-001 is COM-001's content source (architectural peer). COM-001 elaborates BIZ-001 content but must not require BIZ-001 changes. No BIZ-001 modification anticipated.                                                                                                                                  |
| CON-001       | **No change**          | Constitutional document. COM-001 must conform to CON-001, not modify it.                                                                                                                                                                                                                                 |
| CAP Framework | **No change**          | CAP-001/002/004 unchanged. COM-001 operates strictly within the Commercial capability.                                                                                                                                                                                                                   |

---

## 3. Impact Detail by Document

### 3.1 USR-001 — Metadata Alignment

| Impact               | Detail                                                                                                                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Commercial personas  | COM-001 defines commercial roles USR-001 may reference: Payer (individual), Organisation Administrator (commercial settings per CON-001 §8), Finance/Procurement contact (enterprise) |
| No structural impact | USR-001's user groups (Independent Publisher, Organisation Publisher, Administrator, Contributor, Reader) do not change                                                               |
| Action               | During WP-05 (USR-001), reference COM-001's commercial roles where user needs intersect commercial actions (purchasing, wallet management, approvals)                                 |

### 3.2 JNY-001 — Minor Alignment

| Impact                     | Detail                                                                                                                                                        |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Journeys directly affected | J5 (Preview Publication) — will include cost preview; J6 (Acquire Publishing Capacity) — will include bundle purchase, wallet top-up, organisation allocation |
| Journeys potentially added | Enterprise procurement journey (if FD-11 recommended option A), hosting renewal journey (per FD-07), inactive-account reconciliation (per FD-01)              |
| No journey list change     | Core 10 journeys (J1-J10) remain valid; detail is enriched                                                                                                    |
| Action                     | During WP-06 (JNY-001), incorporate COM-001 mechanics into J5/J6; add enterprise/renewal journeys per Founder decisions                                       |

### 3.3 FEA-001 — Minor Alignment

| Impact                            | Detail                                                                                                                                                                                       |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Commercial feature domain         | FEA-001 "D. Commercial" (Wallet, Credits, Transactions, Purchase History) must expand to cover COM-001's surface: entitlements, add-ons, renewal, country configuration, enterprise features |
| Domain list                       | FEA-001's non-PA-001 domains (Administration) remain a WP-07 concern per DF-002                                                                                                              |
| No structural impact before WP-07 | FEA-001 is L1 skeleton; expansion is its own WP                                                                                                                                              |
| Action                            | During WP-07 (FEA-001), align Commercial feature domain to PA-001's Commercial domain + COM-001's Rule surface                                                                               |

### 3.4 REQ-001 — Minor Alignment

| Impact                | Detail                                                                                                                        |
| --------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Existing requirements | FR-007 (manage publishing credits) remains; will be decomposed into fuller commercial requirements during WP-08               |
| New requirement areas | Cost preview, approval, entitlement, renewal, add-on, enterprise, country-configuration requirements will derive from COM-001 |
| Traceability          | REQ-001 must trace each requirement to a COM-001 commercial rule + PA-001 domain + FEA-001 feature                            |
| Action                | During WP-08 (REQ-001), derive commercial requirements from expanded COM-001                                                  |

### 3.5 DAT-001 — Minor Alignment (Phase 3)

| Impact        | Detail                                                                                                                  |
| ------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Entities      | Wallet, Credit, Payment, Transaction, Entitlement, Credit-Ledger entities per CAP-004 and PA-001 §4.4                   |
| Rules         | COM-001's commercial rules (non-expiry, reversal, approval) constrain entity behaviour                                  |
| No change now | DAT-001 is L0 (Planned); created in Phase 3. COM-001's expansion informs DAT-001 but does not require a current change. |

### 3.6 ARC-001 — Minor Alignment (Phase 3)

| Impact                 | Detail                                                                                                             |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Implementation surface | Payment gateway, ledger, wallet, credit-consumption services implemented in ARC-001                                |
| Boundary               | COM-001 defines commercial strategy and rules; ARC-001 implements. COM-001 §9 correctly defers provider selection. |
| No change now          | ARC-001 is L0 (Planned). Boundary preserved.                                                                       |

### 3.7 IMP-001 — No Change

IMP-001 is the terminal engineering-delivery document. COM-001 adds commercial-definition content; no new implementation-programme requirement is introduced at this stage.

### 3.8 MP-001 — Metadata Alignment (at closure)

| Impact                | Detail                                                            |
| --------------------- | ----------------------------------------------------------------- |
| Document Register     | COM-001 row: version 0.1→0.4, maturity L1→L2, status Active Draft |
| Parents               | Remain `PA-001 (architectural); BIZ-001 (content)` — no change    |
| Dashboard             | Foundation completion 3/8→4/8; COM-001 added to complete list     |
| Work Package Register | WP-04: Planned→Closed at closure                                  |
| Timing                | Applied at COM-001 completion/closure, not during planning        |

---

## 4. No-Redesign Confirmation

**No downstream document requires major redesign** as a result of COM-001 expansion.

Reasoning:

- The 6-domain PA-001 architecture is unchanged.
- COM-001 operates strictly within the Commercial capability (no new L1).
- Downstream skeletons (USR-001, JNY-001, FEA-001, REQ-001) are L1 and will incorporate COM-001 content during their own expansion WPs.
- DAT-001 and ARC-001 are L0 (Planned) and will incorporate COM-001 rules during Phase 3.
- CON-001, BIZ-001, CAP Framework require no changes.

---

## 5. Dependency Integrity Confirmation

| Check                             | Result                                                            |
| --------------------------------- | ----------------------------------------------------------------- |
| Architectural hierarchy preserved | Peer branches (BIZ-001, COM-001, USR-001 under PA-001) unaffected |
| Content dependency recorded       | COM-001 → BIZ-001 (content) maintained in expanded document       |
| No circular dependency            | No downstream document feeds back into COM-001 architecturally    |
| No new L1 capability              | COM-001 confined to Commercial capability                         |
| Downstream consumers documented   | Each consumer identified by classification and action             |

---

## 6. Summary

| Classification     | Documents                                   |
| ------------------ | ------------------------------------------- |
| No change          | CON-001, BIZ-001, CAP Framework, IMP-001    |
| Metadata alignment | MP-001 (at closure), USR-001                |
| Minor alignment    | JNY-001, FEA-001, REQ-001, DAT-001, ARC-001 |
| Major redesign     | **None**                                    |

COM-001 expansion is safely contained. No downstream document needs redesign. Each downstream impact is deferred to the document's own work package.

---
