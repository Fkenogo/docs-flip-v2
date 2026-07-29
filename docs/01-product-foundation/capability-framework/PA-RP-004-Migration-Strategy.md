# PA-RP-004 — Migration Strategy

**Task:** DOCSFLIP-PA-001R  
**Date:** 2026-07-29

---

## 1. Migration Overview

**Current State:** PA-001 v0.1, L1 Skeleton — 10 flat domains, 3 invented, 1 capability gap.

**Target State:** PA-001 refactored — 6 tiered domains matching CAP-001's Level 1 capabilities.

---

## 2. Phase 1 — Structural Refactoring

**Objective:** Align PA-001's domain set with CAP-001. No content expansion.

| Step | Action                                                                                                                           | Validation                          |
| ---- | -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| P1.1 | Remove Integrations domain — defer to ARC-001                                                                                    | CAP-001 §5 compliance               |
| P1.2 | Remove Administration domain — workspace governance to Organisations; technical concerns to ARC-001                              | CAP-005 capability retirement rules |
| P1.3 | Remove Platform Services domain name — notifications/audit/config deferred to ARC-001                                            | CAP-001 §5 compliance               |
| P1.4 | Merge Publishing + Publication Management + Distribution → Publications domain with Creation/Management/Distribution sub-domains | CAP-001 §2, CAP-002                 |
| P1.5 | Rename Organisation → Organisations                                                                                              | CAP-001 §2 naming                   |
| P1.6 | Add Reader Experience domain with Reading, Navigation, Accessibility, Search, Reader Preferences sub-domains                     | CAP-001 §2, CAP-002                 |
| P1.7 | Adopt Core/Supporting tier model                                                                                                 | CAP-001 capability hierarchy        |
| P1.8 | Update §1 Purpose to "elaborates the canonical capability model"                                                                 | CAP-000 §4                          |
| P1.9 | Update §7 Foundational Decisions to reflect elaboration role                                                                     | CAP-001 §7, CAP-005                 |

**Dependencies:** None. All structural changes are within PA-001.

**Validation Checkpoint:** PA-001 has exactly 6 domains matching CAP-001. No invented domains.

---

## 3. Phase 2 — Domain Content

**Objective:** For each of the 6 domains, write purpose, capability owner, business assets, bounded contexts, responsibilities, and relationships per PA-RP-003 blueprint.

| Step | Domain            | Tasks                                                                          |
| ---- | ----------------- | ------------------------------------------------------------------------------ |
| P2.1 | Identity          | Write domain definition, sub-domains, bounded context, assets, relationships   |
| P2.2 | Organisations     | Write domain definition, sub-domains, bounded context, assets, relationships   |
| P2.3 | Publications      | Write domain definition, 3 sub-domains, bounded context, assets, relationships |
| P2.4 | Commercial        | Write domain definition, sub-domains, bounded context, assets, relationships   |
| P2.5 | Reader Experience | Write domain definition, sub-domains, bounded context, assets, relationships   |
| P2.6 | Analytics         | Write domain definition, sub-domains, bounded context, assets, relationships   |

**Dependencies:** Phase 1 structural refactoring complete.

**Validation Checkpoint:** All 6 domains have complete definitions. All trace to CAP-001/002/003/004.

---

## 4. Phase 3 — Relationship and Traceability Model

**Objective:** Replace adjacency table with lifecycle flow, dependency model, and downstream traceability.

| Step | Action                                                                                                               |
| ---- | -------------------------------------------------------------------------------------------------------------------- |
| P3.1 | Create lifecycle flow diagram (Identity → Organisations → Publications → Commercial + Reader Experience → Analytics) |
| P3.2 | Create dependency model                                                                                              |
| P3.3 | Update downstream traceability: BIZ-001, COM-001, USR-001, JNY-001, FEA-001, REQ-001, DAT-001, ARC-001, IMP-001      |

**Dependencies:** Phase 2 complete.

**Validation Checkpoint:** Relationship model covers full lifecycle. All downstream documents have domain mappings.

---

## 5. Risks

| Risk                                                        | Severity | Mitigation                                                                               |
| ----------------------------------------------------------- | -------- | ---------------------------------------------------------------------------------------- |
| Domain name changes break downstream references             | Medium   | Update downstream document metadata in Phase 3                                           |
| Publications merge loses conceptual nuance                  | Low      | Preserve Creation/Management/Distribution as named sub-domains                           |
| Reader Experience domain lacks historical content in PA-001 | Low      | CAP-002 provides Level 2/3 decomposition; CON-001 provides constitutional basis          |
| WP-02 redefinition causes programme disruption              | Low      | MP-001 update captures new scope; existing WP-02 artefacts remain as historical analysis |

---

## 6. Dependencies

| Phase   | Depends On                                             | Blocks                                           |
| ------- | ------------------------------------------------------ | ------------------------------------------------ |
| Phase 1 | CAP Framework authoritative (Validation Gate approved) | Phase 2                                          |
| Phase 2 | Phase 1 complete                                       | Phase 3                                          |
| Phase 3 | Phase 2 complete                                       | PA-001 content expansion, downstream realignment |

---

## 7. Validation Checkpoints

| Checkpoint           | After Phase | Criteria                                                      |
| -------------------- | ----------- | ------------------------------------------------------------- |
| Structural alignment | 1           | 6 domains, no invented domains, tiered model, purpose updated |
| Domain content       | 2           | All 6 domains fully defined per blueprint                     |
| Relationship model   | 3           | Lifecycle + dependency + traceability complete                |
| Final                | 3           | PA-001 v0.2, L2 Expanded, matched to CAP-001                  |
