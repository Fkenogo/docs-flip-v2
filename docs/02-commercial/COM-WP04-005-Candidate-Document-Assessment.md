# COM-WP04-005 — Candidate Document Assessment

**WP:** WP-04 — Commercial Architecture Planning and Gap Analysis  
**Phase:** Planning / Analysis Only  
**Date:** 2026-08-06  
**Status:** Founder Authorised

---

## 1. Purpose

This report reviews the three Candidate Register entries relevant to COM-001 — PRC-001 (Pricing Architecture), PAY-001 (Payment Strategy), PUB-001 (Publication Output Rules) — and recommends whether each should remain a candidate, be absorbed into COM-001, be approved as a future specialist document, be rejected, or require further evidence.

**No candidate files were created. No Candidate Register was modified.**

---

## 2. Candidate Review Context

The Candidate Register (MP-001 §9) governs all proposed documents. Operating Rule 7: "All candidate documents are governed by the Candidate Register until Founder approval. Candidate identifiers must not be treated as permanent repository documents, added to the active dependency model, or created as files before approval."

COM-001's skeleton §4 states: "Each component may be expanded into its own specialist document if required." This establishes the principle that commercial components may later split into specialist documents.

---

## 3. PRC-001 — Pricing Architecture

| Attribute                                         | Assessment                                                                                                    |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| Current candidate status                          | Proposed — future sub-document of COM-001                                                                     |
| Scope (as noted)                                  | Pricing Architecture                                                                                          |
| Does the authoritative baseline require this now? | No — COM-001 §8 (Pricing Architecture) is a skeleton component that COM-001 must expand first                 |
| What COM-001 must contain                         | Pricing architecture principles, base vs add-on separation, price-point governance, segment pricing framework |
| When PRC-001 could justify separation             | Only after COM-001 reaches L2 and pricing complexity demonstrates a need for a dedicated document             |
| Risk of premature creation                        | Would duplicate COM-001's Pricing Architecture section; violates Candidate Register rule                      |

**Recommendation: REMAIN A CANDIDATE.** PRC-001 stays in the Candidate Register. COM-001 must absorb Pricing Architecture as a full section during expansion. Reassess PRC-001 only after COM-001 closure, when pricing complexity and price-point governance needs are evident.

---

## 4. PAY-001 — Payment Strategy

| Attribute                                         | Assessment                                                                                                                                            |
| ------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Current candidate status                          | Proposed — future sub-document of COM-001                                                                                                             |
| Scope (as noted)                                  | Payment Strategy                                                                                                                                      |
| Does the authoritative baseline require this now? | No — COM-001 §9 (Payment Strategy) is a skeleton component that COM-001 must expand first                                                             |
| What COM-001 must contain                         | Payment method strategy, country configuration, currency/tax frameworks, invoicing/procurement, provider-abstraction boundary                         |
| When PAY-001 could justify separation             | After COM-001 L2, when payment-method complexity per country and payment-provider integration decisions surface (likely near ARC-001/technical phase) |
| Risk of premature creation                        | Would fragment payment strategy across two documents during COM-001 expansion                                                                         |

**Recommendation: REMAIN A CANDIDATE.** PAY-001 stays in the Candidate Register. COM-001 must absorb Payment Strategy as a full section. Reassess PAY-001 during Technical Definition (Phase 3) when ARC-001 work reveals payment-provider integration complexity.

---

## 5. PUB-001 — Publication Output Rules

| Attribute                                         | Assessment                                                                                                                                      |
| ------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Current candidate status                          | Proposed — future sub-document of COM-001                                                                                                       |
| Scope (as noted)                                  | Publication Output Rules                                                                                                                        |
| Does the authoritative baseline require this now? | No — but Publication Output Model is a core COM-001 component (§6) that must be fully expanded                                                  |
| What COM-001 must contain                         | Base publication cost model, page allowance, additional-page pricing, output add-ons, what constitutes a publication output, republishing rules |
| When PUB-001 could justify separation             | After COM-001 L2, if the publication output model grows complex enough that COM-001 becomes unwieldy                                            |
| Risk of premature creation                        | Would split the core commercial value model from COM-001's centre                                                                               |

**Recommendation: REMAIN A CANDIDATE.** PUB-001 stays in the Candidate Register. Publication Output Model is the **centre** of COM-001 — it should be fully developed within COM-001 first. Reassess PUB-001 only after COM-001 closure demonstrates whether the output model warrants a specialist document.

---

## 6. Summary Decision Table

| Candidate                          | Recommendation       | Rationale                                      | Reassessment Trigger           |
| ---------------------------------- | -------------------- | ---------------------------------------------- | ------------------------------ |
| PRC-001 — Pricing Architecture     | **Remain candidate** | COM-001 must absorb pricing architecture first | After COM-001 closure          |
| PAY-001 — Payment Strategy         | **Remain candidate** | COM-001 must absorb payment strategy first     | Phase 3 (Technical Definition) |
| PUB-001 — Publication Output Rules | **Remain candidate** | Output model is COM-001's centre               | After COM-001 closure          |
| EXP-001 — Product Experience       | Not assessed here    | Non-commercial candidate; outside WP-04 scope  | —                              |

---

## 7. No-Action Confirmation

- No candidate document was created.
- No Candidate Register entry was modified, removed, or promoted.
- No candidate identifier was used as a permanent document or file.
- No candidate was added to the active dependency model.
- The only action is the recommendation above, which the Founder may accept, modify, or reject.

---

## 8. Evidence Basis

| Finding                                                                       | Evidence                         |
| ----------------------------------------------------------------------------- | -------------------------------- |
| Candidates are "future sub-document of COM-001"                               | MP-001 §9 Candidate Register     |
| "Each component may be expanded into its own specialist document if required" | COM-001 §4                       |
| Candidate documents must not be created before approval                       | MP-001 Operating Rule 7          |
| COM-001 §8 Pricing / §9 Payment / §6 Output Model must be expanded            | COM-WP04-001 §4, COM-WP04-004 §2 |

---
