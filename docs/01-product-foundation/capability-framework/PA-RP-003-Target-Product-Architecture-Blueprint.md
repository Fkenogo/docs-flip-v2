# PA-RP-003 — Target Product Architecture Blueprint

**Task:** DOCSFLIP-PA-001R  
**Date:** 2026-07-29  
**Authority:** CAP-001, CAP-002, CAP-003, CAP-004

---

## 1. Target Domain Set

6 domains, matching CAP-001's 6 Level 1 capabilities:

| Tier       | Domain            | CAP-001 Reference | Level 2 Sub-domains (CAP-002)                                                                                                                                                                                                        |
| ---------- | ----------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Core       | Identity          | CAP-001 §2        | Registration, Authentication, Profile, Account Lifecycle, Personal Preferences                                                                                                                                                       |
| Core       | Organisations     | CAP-001 §2        | Organisation Management, Workspace Management, Membership, Roles & Permissions, Invitations, Collaboration Settings                                                                                                                  |
| Core       | Publications      | CAP-001 §2        | Creation (Upload, Validation, Conversion, Preview, Publish), Management (Hosting, Metadata, Ownership, Availability, Visibility, Lifecycle, Archive, Restore, Delete), Distribution (Share Links, Embeds, QR Codes, Access Policies) |
| Core       | Commercial        | CAP-001 §2        | Wallet, Credits, Payments, Entitlements, Publication Outputs                                                                                                                                                                         |
| Supporting | Reader Experience | CAP-001 §2        | Reading, Navigation, Search, Accessibility, Reader Preferences                                                                                                                                                                       |
| Supporting | Analytics         | CAP-001 §2        | Publication Metrics, Reader Behaviour, Publisher Insights, Commercial Reporting                                                                                                                                                      |

---

## 2. Domain Definitions

### Identity (Core)

**Purpose:** Individual account management, authentication, and credential lifecycle.

**Capability Owner:** Identity (CAP-001)  
**Business Assets:** User (CAP-004)  
**Bounded Context:** Identity owns Users, credentials, and profiles. Does not own organisational membership (Organisations). Does not own reader sessions (Reader Experience).

**Responsibilities:** User registration, login/logout, password management, profile settings, account recovery, personal preferences, credential security.

**Relationships:** Provides authentication to Organisations. Provides identity context to Publications. Provides profile data to Reader Experience. Consumed by all domains that require authentication.

---

### Organisations (Core)

**Purpose:** Organisation workspaces, team structures, and workspace-level governance.

**Capability Owner:** Organisations (CAP-001)  
**Business Assets:** Organisation, Workspace, Membership (CAP-004)  
**Bounded Context:** Organisations owns workspaces and organisational membership. Does not own individual user accounts (Identity). Does not own commercial entitlements (Commercial). Does not own publications directly (Publications owns publications; Organisations owns the organisational context).

**Responsibilities:** Workspace creation, team management, member invitations, role assignment, workspace-level permissions, organisation branding, collaboration settings.

**Relationships:** Depends on Identity for user authentication. Provides organisational context to Publications and Commercial. Workspace-level roles constrain publishing and commercial actions.

---

### Publications (Core)

**Purpose:** The full lifecycle of digital publications — creation, management, and distribution.

**Capability Owner:** Publications (CAP-001)  
**Business Assets:** Publication, Publication Metadata, Publication Access (CAP-004) — "The Publication remains the primary business asset of Docsflip" (CAP-004)  
**Bounded Context:** Publications owns the publication lifecycle from upload to archival. Does not own commercial monetisation (Commercial). Does not own how publications are read (Reader Experience). Does not own how publications are measured (Analytics).

**Responsibilities:** PDF upload, validation, conversion/flipbook generation, preview, publish action, hosting, lifecycle states (active/renewal due/suspended/archived/deleted), metadata management, ownership tracking, availability/visibility control, sharing, embedding, QR codes, access policies.

**Relationships:** Depends on Identity for publisher identity. Consumed by Commercial for monetisation events. Provides publications to Reader Experience. Generates events for Analytics.

---

### Commercial (Core)

**Purpose:** The commercial engine — credits, wallets, payments, entitlements, and publication output monetisation.

**Capability Owner:** Commercial (CAP-001)  
**Business Assets:** Wallet, Credit, Payment (CAP-004)  
**Bounded Context:** Commercial owns the commercial value system. Does not own publication lifecycle (Publications). Does not own business strategy or pricing policy (BIZ-001, COM-001 define rules; PA-001 defines capability). Country configuration for payments is a Commercial sub-concern.

**Responsibilities:** Wallet management, credit purchase, credit consumption, payment initiation, entitlement management, publication output selection and pricing display, transaction history.

**Relationships:** Monetises Publications. Depends on Publications for publish events. Provides commercial data to Analytics. Rules defined in COM-001.

---

### Reader Experience (Supporting)

**Purpose:** Publication consumption — reading, navigation, accessibility, and reader interaction.

**Capability Owner:** Reader Experience (CAP-001)  
**Business Assets:** Reader Session (CAP-004)  
**Bounded Context:** Reader Experience owns the reading interaction. Does not own publication creation or distribution (Publications). Does not own sharing mechanisms (Publications → Distribution sub-domain).

**Responsibilities:** Flipbook viewer, page navigation, zoom, search within publication, mobile-responsive viewing, accessibility features (screen reader, keyboard navigation), reader preferences.

**Relationships:** Consumes publications from Publications. Generates reader behaviour events for Analytics. Depends on Publications for access control (public/restricted visibility).

---

### Analytics (Supporting)

**Purpose:** Publication performance measurement and business insight.

**Capability Owner:** Analytics (CAP-001)  
**Business Assets:** Analytics Event, Analytics Report (CAP-004)  
**Bounded Context:** Analytics measures outcomes. Does not own the events it measures (Publications, Reader Experience, Commercial). Does not define what should be measured (that is a capability concern of the source domain).

**Responsibilities:** Publication performance metrics, reader behaviour tracking, publisher insights, commercial reporting, geographic distribution data.

**Relationships:** Receives events from Publications, Reader Experience, and Commercial. Provides reports to publisher-facing and operator-facing consumers.

---

## 3. Relationship Model

### Lifecycle Flow

```text
Identity ──► Organisations ──► Publications ──► Commercial ──► Publications (publish)
                                            │
                                            ▼
                                     Reader Experience ──► Analytics
```

### Dependency Model

```text
Identity ← used by Organisations, Publications, Commercial
Organisations ← used by Publications, Commercial
Publications ← consumed by Commercial, Reader Experience, Analytics
Commercial ← monetises Publications
Reader Experience ← depends on Publications
Analytics ← depends on Publications, Reader Experience, Commercial
```

---

## 4. Cross-Cutting Concerns Deferred to ARC-001

Per CAP-001 §5:

| Concern                | Disposition                          |
| ---------------------- | ------------------------------------ |
| Notifications          | ARC-001 — technical delivery concern |
| Audit trail            | ARC-001 — technical infrastructure   |
| Platform configuration | ARC-001 — technical operations       |
| APIs                   | ARC-001 — technical delivery         |
| Cloud storage          | ARC-001 — infrastructure             |
| Databases              | ARC-001 — infrastructure             |
| Integrations           | ARC-001 — technical architecture     |

---

## 5. Validation

| Check                                            | Result |
| ------------------------------------------------ | ------ |
| 6 domains match CAP-001's 6 Level 1 capabilities | ✅     |
| All domain definitions trace to CAP documents    | ✅     |
| No invented domains                              | ✅     |
| Bounded contexts defined per CAP-003             | ✅     |
| Business assets mapped per CAP-004               | ✅     |
| No implementation decisions                      | ✅     |
