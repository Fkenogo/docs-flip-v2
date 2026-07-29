# PF-002 — Programme Dependency Update Report

**Task:** DOCSFLIP-PF-001 Phase A  
**Date:** 2026-07-29  
**Status:** Analytical — no programme changes applied

---

## 1. Current Dependency Model (MP-001 §7)

### 1.1 Current Execution Sequence

```text
MP-001 → CON-001 → PA-001 → BIZ-001 → COM-001 → USR-001 → JNY-001 → FEA-001 → REQ-001 → DAT-001 → ARC-001 → IMP-001
```

### 1.2 Current Architectural Dependency Model

```text
CON-001 → PA-001 → {BIZ-001, COM-001, USR-001} → JNY-001 → FEA-001 → REQ-001 → DAT-001 → ARC-001 → IMP-001
```

---

## 2. Proposed Dependency Model (Post-Integration)

### 2.1 Proposed Execution Sequence

```text
MP-001 → CON-001 → CAP-000 → {CAP-001, CAP-002, CAP-003, CAP-004, CAP-005} → PA-001 → BIZ-001 → COM-001 → USR-001 → JNY-001 → FEA-001 → REQ-001 → DAT-001 → ARC-001 → IMP-001
```

**Rationale:** CAP-000 defines the framework. CAP-001 through CAP-005 provide the canonical capability model, maps, interactions, asset model, and governance standard. These must be established before PA-001 can elaborate capabilities.

### 2.2 Proposed Architectural Dependency Model

```text
CON-001
    │
    ▼
CAP-001 (Canonical Capability Model)
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

**Key change:** CAP-001 inserted between CON-001 and PA-001. PA-001's constitutional constraints (CAP-001 §7, CAP-005) change from "PA-001 defines domains" to "PA-001 elaborates capabilities."

---

## 3. MP-001 Sections Requiring Update (Phase B)

| MP-001 Section                  | Change Required                                                                                                      |
| ------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| §7.1 (Execution Sequence)       | Insert CAP-000 through CAP-005 between CON-001 and PA-001                                                            |
| §7.2 (Architectural Dependency) | Insert CAP-001 between CON-001 and PA-001; update key observations                                                   |
| §7.2 (Key Observations)         | Add note: "CAP-001 defines the canonical capability model. PA-001 elaborates it without inventing new capabilities." |
| §8 (Document Register)          | Add 6 CAP documents: CAP-000 (L1 Skeleton), CAP-001 through CAP-005 (L1 Skeleton). Parent: CON-001.                  |
| §15 (Programme Roadmap)         | Consider whether CAP documents require work packages for expansion                                                   |
| §16 (Repository Dashboard)      | Update planned document count: 18 permanent + 1 legacy                                                               |

---

## 4. Document Register Proposed Additions (Phase B)

| ID      | Title                                      | Area       | Maturity      | Parent Documents | Repository Path                                    |
| ------- | ------------------------------------------ | ---------- | ------------- | ---------------- | -------------------------------------------------- |
| CAP-000 | Capability Framework                       | Foundation | L1 (Skeleton) | MP-001, CON-001  | `docs/01-product-foundation/capability-framework/` |
| CAP-001 | Canonical Capability Model                 | Foundation | L1 (Skeleton) | CAP-000          | `docs/01-product-foundation/capability-framework/` |
| CAP-002 | Capability Maps                            | Foundation | L1 (Skeleton) | CAP-001          | `docs/01-product-foundation/capability-framework/` |
| CAP-003 | Capability Interactions & Bounded Contexts | Foundation | L1 (Skeleton) | CAP-001          | `docs/01-product-foundation/capability-framework/` |
| CAP-004 | Business Asset Model                       | Foundation | L1 (Skeleton) | CAP-001          | `docs/01-product-foundation/capability-framework/` |
| CAP-005 | Capability Governance Standard             | Foundation | L1 (Skeleton) | CAP-000          | `docs/01-product-foundation/capability-framework/` |

---

## 5. Document Relationship Updates Required (Phase B)

| Document                | Current Parents           | Changed To                                      |
| ----------------------- | ------------------------- | ----------------------------------------------- |
| PA-001                  | MP-001, CON-001           | MP-001, CON-001, CAP-001                        |
| CON-001 §10 (Ecosystem) | Lists PA-001 and children | Add CAP-000 as intermediate child before PA-001 |

---

## 6. Phase B Blockers

- CAP-001, CAP-002, CAP-003 not yet in target directory.
- CAP document statuses not yet transitioned from "Draft" to "Active."
- No MP-001 registration of CAP documents.
- No Founder approval for dependency chain insertion.

---

## 7. Conclusion

The dependency update is well-defined and non-disruptive. The Capability Framework inserts cleanly between CON-001 and PA-001. Phase B implementation is blocked pending Founder approval and CAP document relocation.
