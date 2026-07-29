# PF-004 — PA-001 Readiness Assessment

**Task:** DOCSFLIP-PF-001 Phase A  
**Date:** 2026-07-29  
**Status:** Analytical — PA-001 not modified

---

## 1. Question Under Assessment

Does PA-001 currently:

**(a) invent capabilities** — define its own business capability concepts, or  
**(b) expand capabilities** — elaborate capabilities already defined elsewhere?

Per CAP-000 §4: "Product Architecture elaborates capabilities but does not invent them."

---

## 2. Current PA-001 Domain-to-Capability Mapping

| PA-001 Domain (v0.1)   | CAP-001 Capability          | Alignment                                                                 |
| ---------------------- | --------------------------- | ------------------------------------------------------------------------- |
| Identity               | Identity                    | ✅ Aligned — same name, similar decomposition                             |
| Organisation           | Organisations               | ✅ Aligned — workspaces, teams, governance                                |
| Publishing             | Publications → Creation     | ⚠️ Partial — PA-001 bundles creation, conversion, preview into one domain |
| Publication Management | Publications → Management   | ⚠️ Partial — split from Publications; CAP-001 treats as sub-domain        |
| Distribution           | Publications → Distribution | ✅ Aligned                                                                |
| Commercial             | Commercial                  | ✅ Aligned — credits, wallets, payments                                   |
| Analytics              | Analytics                   | ✅ Aligned                                                                |
| **Administration**     | **None**                    | ❌ **Invented** — no corresponding CAP-001 capability                     |
| **Platform Services**  | **None**                    | ❌ **Invented** — no corresponding CAP-001 capability                     |
| **Integrations**       | **None**                    | ❌ **Invented** — explicitly excluded by CAP-001 §5                       |

---

## 3. Finding

**PA-001 currently invents capabilities.**

Of 10 current domains:

| Category                                | Count | Domains                                                     |
| --------------------------------------- | ----- | ----------------------------------------------------------- |
| Aligned with CAP-001                    | 5     | Identity, Organisation, Distribution, Commercial, Analytics |
| Partial alignment (needs restructuring) | 2     | Publishing, Publication Management                          |
| Invented (no CAP-001 basis)             | 3     | Administration, Platform Services, Integrations             |

### 3.1 Invented Domains Analysis

**Administration** — No constitutional support in CON-001. No CAP-001 capability. "Support" is an operational concern. "Platform administration" capabilities belong to Organisation (workspace governance) or are implementation concerns.

**Platform Services** — Bundles notifications (a genuine capability) with audit and configuration (technical concerns). CAP-001 §5 explicitly excludes "Notification Services" and "Platform Services" from business capabilities. Notifications are a product capability but are not a Level 1 business capability in CAP-001.

**Integrations** — Explicitly excluded by CAP-001 §5: "APIs, Cloud Storage, Databases, Infrastructure, Integrations, Notification Services, Search Engines, Platform Services. These belong in ARC-001."

### 3.2 Alignment Gaps

**Publications split** — CAP-001 defines Publications as a single Level 1 capability with three sub-capabilities: Creation, Management, Distribution. PA-001 splits these across Publishing, Publication Management, and Distribution. This is not invention (the capabilities exist in CAP-001) but is a restructuring that may require Founder review.

**Reader Experience missing** — CAP-001 defines Reader Experience as a Level 1 capability (Reading, Navigation, Accessibility, Search, Reader Preferences). PA-001 has no corresponding domain.

---

## 4. Required Changes to Achieve Alignment

| Priority | Change                                                                             | Constitutional Basis                                                      |
| -------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Critical | Remove Integrations domain                                                         | CAP-001 §5 explicit exclusion                                             |
| Critical | Remove Administration domain or reclassify as operational concern                  | No CAP-001 basis; no CON-001 support                                      |
| High     | Restructure Platform Services — dissolve or narrow to cross-cutting principles     | CAP-001 §5 exclusion; notifications are not a Level 1 business capability |
| High     | Align Publications structure to CAP-001 model (Creation, Management, Distribution) | CAP-001 §2 Level 2 decomposition                                          |
| High     | Add Reader Experience domain                                                       | CAP-001 Level 1 capability                                                |
| Medium   | Update PA-001 purpose statement to reference CAP-001 as source                     | CAP-000 §4                                                                |
| Medium   | Update PA-001 §7 (Foundational Decisions) to reflect capability elaboration role   | CAP-001 §7                                                                |

---

## 5. Impact on WP-02 Founder Decision Agenda

The WP-02 Founder Decision Agenda (DA-001 through DA-012) was prepared before the Capability Framework was integrated. CAP-001 resolves or partially resolves several decisions:

| WP-02 Decision                                | CAP-001 Impact                                                                                                                           |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| DA-001 (Architecture model)                   | Partially resolved — tiered model still needs Founder input, but domain set is now constrained by CAP-001                                |
| DA-002 (Publishing vs Publication Management) | Resolved by CAP-001 — Publications is one capability with Creation, Management, Distribution sub-capabilities                            |
| DA-003 (Administration fate)                  | Resolved by CAP-001 — no corresponding capability; remove or reclassify                                                                  |
| DA-004 (Integrations removal)                 | **Fully resolved by CAP-001 §5** — Integrations belong in ARC-001                                                                        |
| DA-005 (Platform Services)                    | Partially resolved — CAP-001 excludes Platform Services; notifications must find a home                                                  |
| DA-009 (Reader Experience)                    | **Fully resolved by CAP-001** — Reader Experience is a Level 1 capability                                                                |
| DA-004 (Analytics scope)                      | CAP-001 defines Analytics with Publication Analytics, Reader Analytics, Publisher Insights as Level 2                                    |
| DA-010 (Notifications domain)                 | Not resolved — CAP-001 excludes Notification Services from business capabilities. Notifications may be cross-cutting or ARC-001 concern. |

**6 of 12 WP-02 decisions are resolved or substantially informed by CAP-001.** The remaining 6 require Founder determination within the CAP-001 constraints.

---

## 6. Readiness Conclusion

**PA-001 is NOT ready for expansion in its current form.**

It must be restructured to align with the Capability Framework before content expansion can begin. The key blockers are:

1. Three invented domains (Administration, Platform Services, Integrations) must be removed or reclassified.
2. Publications must be restructured to match CAP-001's decomposition.
3. Reader Experience must be added.
4. PA-001's constitutional role must be reframed from "defines the conceptual backbone" to "elaborates the canonical capability model."

**Recommendation:** PA-001 expansion (WP-02) should be deferred until the Capability Framework is formally integrated into the repository (Phase B). WP-02 should then be rescoped as "Align PA-001 to CAP-001" rather than "Expand PA-001 from skeleton."
