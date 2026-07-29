# PA-RP-001 — Current Product Architecture Assessment

**Task:** DOCSFLIP-PA-001R — Refactoring Plan  
**Date:** 2026-07-29  
**Status:** Analytical — no PA-001 changes made

---

## 1. Architectural Intent

The current PA-001 skeleton (v0.1, L1) defines itself as "the conceptual structure of Docsflip … enduring business domains, their responsibilities and relationships without describing technical implementation." It aims to provide "the common vocabulary used by business, commercial, product and engineering documentation."

This intent is partially correct: PA-001 should define architecture domains and vocabulary. However, with the Capability Framework now authoritative, PA-001's role is elaboration, not origination.

---

## 2. Strengths

| Strength                | Detail                                                                       |
| ----------------------- | ---------------------------------------------------------------------------- |
| Technology independence | §3 explicitly declares technology independence and capability-level thinking |
| Downstream traceability | §6 defines clear domain-to-document mappings for BIZ-001 through REQ-001     |
| Relationship model      | §5 provides an adjacency table connecting domains                            |
| Execution context       | §2 embeds PA-001 within the repository hierarchy                             |
| Core coverage           | 7 of 10 domains map to CAP-001 capabilities                                  |

---

## 3. Structural Weaknesses

| Weakness                       | Detail                                                                                                                   |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| Flat domain model              | 10 domains are undifferentiated — no core/supporting/cross-cutting distinction                                           |
| Domain invention               | 3 domains have no CAP-001 basis: Administration, Platform Services, Integrations                                         |
| Publications fragmentation     | CAP-001's single Publications capability is split across Publishing, Publication Management, and Distribution            |
| Missing Reader Experience      | CAP-001 Level 1 capability Reader Experience has no corresponding domain                                                 |
| Relationship model is skeletal | §5 captures adjacency only — no lifecycle, dependency, or authorisation relationships                                    |
| Mixed-capability domains       | Platform Services bundles user-facing notifications with technical audit/configuration                                   |
| Authority gap                  | Purpose statement claims "defines the conceptual structure" — should now say "elaborates the canonical capability model" |
| No domain boundaries defined   | Each domain is a one-line description — no inclusions, exclusions, or bounded contexts                                   |

---

## 4. Constitutional Conflicts

| Conflict                 | CAP Authority                                                                                                       | Detail                                                                         |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| Integrations domain      | CAP-001 §5: "APIs, Cloud Storage, Databases, Infrastructure, Integrations … belong in ARC-001"                      | PA-001 defines Integrations as a product domain — directly contradicts CAP-001 |
| Platform Services domain | CAP-001 §5: "Notification Services, Search Engines, Platform Services … belong in ARC-001"                          | PA-001 bundles notifications, configuration, audit — contradicts CAP-001       |
| Administration domain    | No CAP-001 basis. CON-001 offers no direct constitutional support.                                                  | Invented domain with no capability anchor                                      |
| Publications split       | CAP-001 §2: "Publications → Creation, Management, Distribution" as Level 2 sub-capabilities, not separate domains   | PA-001 splits Publications across 3 top-level domains                          |
| Reader Experience gap    | CAP-001: "Reader Experience → Reading, Navigation, Accessibility, Search, Reader Preferences" as Level 1 capability | PA-001 has no corresponding domain                                             |

---

## 5. Capability Conflicts

Mapping current PA-001 domains to CAP-001 capabilities:

| PA-001 Domain          | CAP-001 Capability          | Conflict                                                   |
| ---------------------- | --------------------------- | ---------------------------------------------------------- |
| Identity               | Identity                    | No conflict — aligned                                      |
| Organisation           | Organisations               | No conflict — aligned                                      |
| Publishing             | Publications → Creation     | Partial — should be sub-domain, not top-level              |
| Publication Management | Publications → Management   | Partial — should be sub-domain, not top-level              |
| Distribution           | Publications → Distribution | Partial — should be sub-domain, not top-level              |
| Commercial             | Commercial                  | No conflict — aligned                                      |
| Analytics              | Analytics                   | No conflict — aligned                                      |
| **Administration**     | None                        | ❌ Capability conflict — no CAP-001 basis                  |
| **Platform Services**  | None                        | ❌ Capability conflict — explicitly excluded by CAP-001 §5 |
| **Integrations**       | None                        | ❌ Capability conflict — explicitly excluded by CAP-001 §5 |
| _(missing)_            | Reader Experience           | ❌ Capability gap — Level 1 capability not represented     |

---

## 6. Assessment Summary

**PA-001 is structurally misaligned with the Capability Framework.** It requires refactoring to:

1. Remove 3 invented domains (Administration, Platform Services, Integrations)
2. Restructure Publications into a single domain with Creation, Management, Distribution as sub-domains
3. Add Reader Experience as a domain
4. Adopt a tiered model (Core / Supporting / Cross-cutting)
5. Define bounded contexts for each domain
6. Replace relationship adjacency table with lifecycle + dependency model
7. Update purpose statement and foundational decisions to reflect elaboration role

**PA-001 is not ready for content expansion.** It requires structural refactoring before any domain-level content can be written.
