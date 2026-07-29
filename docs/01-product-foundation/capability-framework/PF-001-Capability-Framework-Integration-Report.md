# PF-001 — Capability Framework Integration Report

**Task:** DOCSFLIP-PF-001 Phase A — Repository Preparation  
**Date:** 2026-07-29  
**Status:** Analytical — no integration performed  
**Phase:** Phase A — Repository Preparation (Phase B requires Founder approval and CAP document provision)

---

## 1. Current Repository State

### 1.1 CAP Documents Discovered

| Document | Current Location                                                                                          | Status                                                    |
| -------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| CAP-000  | `docs/01-product-foundation/capability-framework/DOCSFLIP-CAP-000-Capability-Framework-v0.1.md`           | Founder Draft — in target location                        |
| CAP-001  | `docs/01-product-foundation/DOCSFLIP-CAP-001-Canonical-Capability-Model-v1.0-Founder-Candidate.md`        | Founder Candidate — in parent directory, needs relocation |
| CAP-002  | `docs/01-product-foundation/DOCSFLIP-CAP-002-Capability-Maps-v0.1.md`                                     | Founder Draft — in parent directory, needs relocation     |
| CAP-003  | `docs/01-product-foundation/DOCSFLIP-CAP-003-Capability-Interactions-and-Bounded-Contexts-v0.1.md`        | Founder Draft — in parent directory, needs relocation     |
| CAP-004  | `docs/01-product-foundation/capability-framework/DOCSFLIP-CAP-004-Business-Asset-Model-v0.1.md`           | Founder Draft — in target location                        |
| CAP-005  | `docs/01-product-foundation/capability-framework/DOCSFLIP-CAP-005-Capability-Governance-Standard-v0.1.md` | Founder Draft — in target location                        |

**Observation:** CAP-001, CAP-002, CAP-003 are in `docs/01-product-foundation/` root. CAP-000, CAP-004, CAP-005 are in the target `capability-framework/` directory. Phase B must relocate CAP-001, CAP-002, CAP-003 into `capability-framework/`.

### 1.2 Target Structure

Per task specification, all CAP documents should reside in:

```text
docs/
└── 01-product-foundation/
    └── capability-framework/
        ├── DOCSFLIP-CAP-000-Capability-Framework.md
        ├── DOCSFLIP-CAP-001-Canonical-Capability-Model.md
        ├── DOCSFLIP-CAP-002-Capability-Maps.md
        ├── DOCSFLIP-CAP-003-Capability-Interactions-and-Bounded-Contexts.md
        ├── DOCSFLIP-CAP-004-Business-Asset-Model.md
        └── DOCSFLIP-CAP-005-Capability-Governance-Standard.md
```

---

## 2. Capability Framework Summary

### 2.1 Framework Structure

CAP-000 defines the framework. Five subsidiary documents:

| Document | Purpose                                                                                 |
| -------- | --------------------------------------------------------------------------------------- |
| CAP-001  | Canonical Capability Model — 6 Level 1 capabilities with decomposition                  |
| CAP-002  | Capability Maps — Level 2 and Level 3 decomposition                                     |
| CAP-003  | Capability Interactions & Bounded Contexts — interaction boundaries and asset ownership |
| CAP-004  | Business Asset Model — 13 canonical business assets with single authoritative owners    |
| CAP-005  | Capability Governance Standard — rules for creating, modifying, retiring capabilities   |

### 2.2 Canonical Capability Model (CAP-001)

**6 Level 1 Capabilities:**

| Capability        | Level 2 Decomposition                                                |
| ----------------- | -------------------------------------------------------------------- |
| Identity          | Registration, Authentication, Profile, Account Lifecycle             |
| Organisations     | Workspace Management, Membership, Roles & Permissions, Collaboration |
| Publications      | Creation, Management, Distribution                                   |
| Reader Experience | Reading, Navigation, Accessibility, Search, Reader Preferences       |
| Commercial        | Wallet, Credits, Payments, Entitlements, Publication Outputs         |
| Analytics         | Publication Analytics, Reader Analytics, Publisher Insights          |

### 2.3 Explicitly Excluded from Business Capabilities (CAP-001 §5)

APIs, Cloud Storage, Databases, Infrastructure, Integrations, Notification Services, Search Engines, Platform Services. These belong in ARC-001.

### 2.4 Constitutional Position (CAP-000 §3)

```text
MP-001
   ↓
CON-001
   ↓
CAP-000 (→ CAP-001 through CAP-005)
   ↓
PA-001
   ↓
USR-001 • COM-001 • DAT-001 • ARC-001 • IMP-001
```

### 2.5 Key Constitutional Rules

- CAP-000 §4: "Product Architecture elaborates capabilities but does not invent them."
- CAP-003: "Business responsibilities may cross capability boundaries through collaboration, but ownership of a business asset shall belong to one capability only."
- CAP-005: "No downstream document may redefine the canonical capability model established by CAP-001 without an approved Founder constitutional decision."
- CAP-001 §7: "PA-001 elaborates this model but does not redefine it."
- CAP-004: "The Publication remains the primary business asset of Docsflip."

---

## 3. Integration Impact Analysis

### 3.1 Repository Changes Required (Phase B)

| Change             | Detail                                                                             |
| ------------------ | ---------------------------------------------------------------------------------- |
| Move CAP-001       | `docs/01-product-foundation/` → `docs/01-product-foundation/capability-framework/` |
| Move CAP-002       | `docs/01-product-foundation/` → `docs/01-product-foundation/capability-framework/` |
| Move CAP-003       | `docs/01-product-foundation/` → `docs/01-product-foundation/capability-framework/` |
| Rename files       | Remove version suffixes and "Founder-Candidate" labels for canonical filenames     |
| Register in MP-001 | Add CAP-000 through CAP-005 to Document Register                                   |

### 3.2 Programme Changes Required (Phase B)

| Change           | Detail                                                         |
| ---------------- | -------------------------------------------------------------- |
| Dependency chain | Insert Capability Framework between CON-001 and PA-001         |
| MP-001 §7.1      | Update execution sequence to include CAP documents             |
| MP-001 §7.2      | Update architectural dependency model                          |
| MP-001 §8        | Add CAP-000 through CAP-005 to Document Register               |
| MP-001 §15       | Update Phase 2 roadmap if CAP expansion requires work packages |

### 3.3 Dependency Updates Required (Phase B)

Current execution sequence:

```text
MP-001 → CON-001 → PA-001 → BIZ-001 → COM-001 → USR-001 → ...
```

Target execution sequence:

```text
MP-001 → CON-001 → CAP-000 through CAP-005 → PA-001 → BIZ-001 → COM-001 → USR-001 → ...
```

### 3.4 Document Relationship Updates Required (Phase B)

| Document | Current Parent          | Proposed Parent Addition                         |
| -------- | ----------------------- | ------------------------------------------------ |
| PA-001   | MP-001, CON-001         | MP-001, CON-001, CAP-001                         |
| COM-001  | MP-001, PA-001, BIZ-001 | (CAP-001 reference in ecosystem section)         |
| USR-001  | MP-001, PA-001          | (CAP-001 reference for user capabilities)        |
| DAT-001  | REQ-001                 | (CAP-001 reference for data ownership)           |
| ARC-001  | DAT-001                 | (CAP-001 reference for technical implementation) |

### 3.5 Cross-Reference Additions Required (Phase B)

| Source Document             | Add Reference To | Reason                                                |
| --------------------------- | ---------------- | ----------------------------------------------------- |
| CON-001 §10 (Ecosystem)     | CAP-000          | Capability Framework is a child of Product Foundation |
| PA-001 §1 (Purpose)         | CAP-001          | PA-001 elaborates capabilities; CAP-001 defines them  |
| PA-001 §4 (Domains)         | CAP-001 §2       | Domain definitions must align with capability model   |
| COM-001 §13 (Relationships) | CAP-001          | Commercial capability is defined in CAP-001           |
| USR-001 §8 (Relationships)  | CAP-001          | User capabilities traced to Identity/Organisations    |

---

## 4. Constitutional Alignment Assessment

### 4.1 CON-001 Alignment with CAP-001

| CON-001 Element                            | CAP-001 Alignment                                                              | Assessment                           |
| ------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------ |
| PH-001 Publishing Outcomes Define Value    | Publications as primary business asset                                         | ✅ Strong — both centre Publications |
| PH-002 Transparency                        | Commercial capability includes Wallet, Credits, Payments                       | ✅ Consistent                        |
| PH-007 Organisations Are First-Class Users | Organisations as Level 1 capability                                            | ✅ Strong                            |
| PP-006 Accessibility                       | Reader Experience → Accessibility as Level 2                                   | ✅ Direct traceability               |
| §7.1 In Scope                              | Publications → Creation, Management, Distribution                              | ✅ Full coverage                     |
| §8 Target Users                            | Identity (publishers), Organisations (workspaces), Reader Experience (readers) | ✅ Complete mapping                  |

**Assessment:** CON-001 is fully aligned with the Capability Framework. No constitutional conflict.

### 4.2 PA-001 Alignment with CAP-001

See PA-001 Readiness Assessment (deliverable 4). Summary: **Not aligned.** PA-001 currently invents domains that CAP-001 excludes and splits Publications across three domains.

---

## 5. Risk Assessment

| Risk                                             | Severity | Detail                                                                                                                                                                                                            |
| ------------------------------------------------ | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| PA-001 domain model conflicts with CAP-001       | High     | PA-001 has 10 domains vs CAP-001's 6 capabilities. Administration, Platform Services, Integrations are excluded by CAP-001 §5.                                                                                    |
| WP-02 audit recommendations partially superseded | Medium   | WP-02 Founder Decision Agenda (DA-001 through DA-012) was prepared before CAP integration. Several decisions are resolved by CAP-001 (Integrations removal, Reader Experience creation, Platform Services split). |
| CAP files scattered across two locations         | Medium   | CAP-001/002/003 in root; CAP-000/004/005 in capability-framework/. Phase B must consolidate.                                                                                                                      |
| Execution sequence disruption                    | Low      | CAP Framework insertion between CON-001 and PA-001 is additive, not disruptive. PA-001 expansion (WP-02) must account for CAP constraints.                                                                        |
| BIZ-001 position unclear                         | Low      | CAP-000 does not explicitly place BIZ-001. BIZ-001 may sit alongside COM-001 and USR-001 under PA-001 as currently defined.                                                                                       |

---

## 6. Required Follow-On Work (Phase B)

1. Relocate CAP-001, CAP-002, CAP-003 into `capability-framework/`.
2. Normalise filenames (remove version suffixes per canonical naming).
3. Register CAP-000 through CAP-005 in MP-001 Document Register.
4. Update MP-001 dependency chain and architectural model.
5. Add capability framework to MP-001 Candidate Register as "Implemented" or transition directly to active documents.
6. Update PA-001 parent metadata and domain definitions.
7. Update cross-references in COM-001, USR-001, DAT-001, ARC-001.
8. Reassess WP-02 Founder Decision Agenda against CAP-001 resolution.
9. Validate no constitutional conflicts.
10. Commit integration milestone.

---

## 7. Phase A Conclusion

**Phase A complete.** All repository preparation analysis has been performed without creating, modifying, or relocating CAP documents. The Capability Framework is understood, impact is analysed, and Phase B integration steps are documented.

**Phase B is blocked** pending Founder approval of this report and explicit authorisation to relocate CAP-001, CAP-002, CAP-003 and update repository governance records.
