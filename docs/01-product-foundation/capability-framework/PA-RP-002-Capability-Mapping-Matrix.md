# PA-RP-002 — Capability Mapping Matrix

**Task:** DOCSFLIP-PA-001R  
**Date:** 2026-07-29  
**Authority:** Capability Framework (CAP-001, CAP-002, CAP-005)

---

## Mapping Table

| #   | Current PA-001 Domain  | CAP-001 Capability               | CAP Reference       | Action                         | Target Domain                                                        | Rationale                                                                                                                                                                         |
| --- | ---------------------- | -------------------------------- | ------------------- | ------------------------------ | -------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| D1  | Identity               | Identity (L1)                    | CAP-001 §2, CAP-002 | **Retain**                     | Identity (Core)                                                      | Direct match. CAP-001 defines Identity with Registration, Authentication, Profile, Account Lifecycle (L2).                                                                        |
| D2  | Organisation           | Organisations (L1)               | CAP-001 §2, CAP-002 | **Retain — Rename**            | Organisations (Core)                                                 | Match to CAP-001 "Organisations" (plural). Add Workspace Management, Membership, Roles & Permissions, Collaboration (L2 per CAP-002).                                             |
| D3  | Publishing             | Publications → Creation (L2)     | CAP-001 §2, CAP-002 | **Merge into Publications**    | Publications (Core)                                                  | Publishing, Publication Management, and Distribution are all L2 sub-capabilities of the CAP-001 Publications L1 capability.                                                       |
| D4  | Publication Management | Publications → Management (L2)   | CAP-001 §2, CAP-002 | **Merge into Publications**    | Publications (Core)                                                  | Hosting, lifecycle, archival are L2 Management sub-capabilities. CAP-004: Publication is the primary business asset.                                                              |
| D5  | Distribution           | Publications → Distribution (L2) | CAP-001 §2, CAP-002 | **Merge into Publications**    | Publications (Core)                                                  | Sharing, embeds, QR codes are L2 Distribution sub-capabilities.                                                                                                                   |
| D6  | Commercial             | Commercial (L1)                  | CAP-001 §2, CAP-002 | **Retain**                     | Commercial (Core)                                                    | CAP-001 defines Wallet, Credits, Payments, Entitlements, Publication Outputs (L2).                                                                                                |
| D7  | Analytics              | Analytics (L1)                   | CAP-001 §2, CAP-002 | **Retain**                     | Analytics (Supporting)                                               | CAP-001 defines Publication Analytics, Reader Analytics, Publisher Insights (L2). CAP-002 adds Commercial Reporting.                                                              |
| D8  | Administration         | None                             | CAP-001 §5, CAP-005 | **Remove**                     | Deferred to ARC-001 / Organisation                                   | No CAP-001 capability. Platform administration is a technical concern. Workspace governance already in Organisations. CAP-001 §5: implementation concerns belong in ARC-001.      |
| D9  | Platform Services      | None                             | CAP-001 §5          | **Split — Remove domain name** | Notifications → ARC-001; Audit → ARC-001; Configuration → Commercial | CAP-001 §5 explicitly excludes Platform Services, Notification Services from business capabilities. Notifications are a cross-cutting concern deferred to ARC-001 per CAP-001 §5. |
| D10 | Integrations           | None                             | CAP-001 §5          | **Remove**                     | Deferred to ARC-001                                                  | CAP-001 §5: "APIs, Cloud Storage, Databases, Infrastructure, Integrations … belong in ARC-001." No redeployment — pure removal.                                                   |
| N1  | _(missing)_            | Reader Experience (L1)           | CAP-001 §2, CAP-002 | **Add**                        | Reader Experience (Supporting)                                       | CAP-001 L1 capability: Reading, Navigation, Accessibility, Search, Reader Preferences (L2). Required per CAP-001.                                                                 |

---

## Summary

| Action              | Count | Domains                                                           |
| ------------------- | ----- | ----------------------------------------------------------------- |
| Retain              | 3     | Identity, Commercial, Analytics                                   |
| Retain — Rename     | 1     | Organisation → Organisations                                      |
| Merge               | 3     | Publishing + Publication Management + Distribution → Publications |
| Remove              | 2     | Administration, Integrations                                      |
| Split — Remove name | 1     | Platform Services                                                 |
| Add                 | 1     | Reader Experience                                                 |

**Current: 10 domains. Target: 6 domains (matching CAP-001's 6 Level 1 capabilities).**
