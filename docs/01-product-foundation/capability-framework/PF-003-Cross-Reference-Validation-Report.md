# PF-003 — Cross-Reference Validation Report

**Task:** DOCSFLIP-PF-001 Phase A  
**Date:** 2026-07-29  
**Status:** Analytical — no changes applied

---

## 1. Current Cross-References Review

### 1.1 References Between Existing Documents

| Source                                                            | Target  | Valid | Notes                                   |
| ----------------------------------------------------------------- | ------- | ----- | --------------------------------------- |
| CON-001 §10 → PA-001                                              | PA-001  | ✅    | Direct parent-child in dependency model |
| CON-001 §10 → BIZ-001                                             | BIZ-001 | ✅    |                                         |
| CON-001 §10 → COM-001                                             | COM-001 | ✅    |                                         |
| CON-001 §10 → USR-001                                             | USR-001 | ✅    |                                         |
| PA-001 §6 → BIZ-001                                               | BIZ-001 | ✅    |                                         |
| PA-001 §6 → COM-001                                               | COM-001 | ✅    |                                         |
| PA-001 §6 → USR-001                                               | USR-001 | ✅    |                                         |
| PA-001 §6 → DAT-001                                               | DAT-001 | ✅    |                                         |
| PA-001 §6 → ARC-001                                               | ARC-001 | ✅    |                                         |
| PA-001 §6 → IMP-001                                               | IMP-001 | ✅    |                                         |
| BIZ-001 §11 → CON-001                                             | CON-001 | ✅    |                                         |
| BIZ-001 §11 → COM-001                                             | COM-001 | ✅    |                                         |
| COM-001 §13 → CON-001                                             | CON-001 | ✅    |                                         |
| COM-001 §13 → BIZ-001                                             | BIZ-001 | ✅    |                                         |
| USR-001 §8 → CON-001, BIZ-001, COM-001, JNY-001, FEA-001, REQ-001 | All     | ✅    |                                         |

### 1.2 Missing Cross-References

| Should Reference | Missing Target | Impact                                                                    |
| ---------------- | -------------- | ------------------------------------------------------------------------- |
| CON-001 §10      | CAP-000        | Low — CAP documents not yet integrated                                    |
| PA-001 §1        | CAP-001        | Medium — PA-001's purpose statement does not acknowledge capability model |
| COM-001 §13      | CAP-001        | Low — Commercial capability defined in CAP-001                            |
| USR-001 §8       | CAP-001        | Low — User capabilities traced to Identity/Organisations                  |

---

## 2. Post-Integration Cross-Reference Map (Phase B)

### 2.1 New References Required

| Source                      | Target                                      | Reason                                                                |
| --------------------------- | ------------------------------------------- | --------------------------------------------------------------------- |
| CON-001 §10 (Ecosystem)     | CAP-000                                     | CAP Framework is child of Product Foundation                          |
| CON-001 §10 (Ecosystem Map) | Insert CAP level between CON-001 and PA-001 |                                                                       |
| PA-001 §1 (Purpose)         | CAP-001                                     | "PA-001 elaborates the canonical capability model defined in CAP-001" |
| PA-001 §4 (Domains)         | CAP-001 §2                                  | Domain definitions aligned with capability model                      |
| PA-001 metadata             | Add CAP-001 to Parent Documents             |                                                                       |
| COM-001 §13 (Relationships) | CAP-001                                     | Commercial capability source                                          |
| USR-001 §8 (Relationships)  | CAP-001                                     | Identity/Organisations capability source                              |

### 2.2 References Made Redundant by CAP-001

| Current Reference                                                                        | Status Post-Integration                                                                                |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| PA-001 §7.1 (Foundational Decision 1: "Product Architecture is the conceptual backbone") | Partially superseded — CAP-001 is the canonical capability backbone; PA-001 elaborates it              |
| PA-001 §7.4 ("Changes to core domains require Founder approval")                         | Reframed — domain changes must align with CAP-001; new Level 1 capabilities require CAP-005 governance |

---

## 3. No Broken References Detected

All existing document references are valid. No document references a non-existent file or a file in the wrong location.

---

## 4. No Circular Dependencies

Current model: `CON-001 → PA-001 → BIZ-001/COM-001/USR-001 → JNY-001/...`

Proposed model: `CON-001 → CAP-001 → PA-001 → BIZ-001/COM-001/USR-001 → ...`

No circular dependencies in either model.

---

## 5. No Orphan Documents

All current documents have parent references. All proposed CAP documents have defined parents (CAP-000 or CAP-001). No document would be orphaned by integration.

---

## 6. Conclusion

Cross-references are structurally sound. The Capability Framework insertion creates clean additive references without breaking existing ones. Phase B must update 4 documents with new cross-references.
