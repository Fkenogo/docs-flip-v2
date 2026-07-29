# DOCSFLIP-FEA-001 — Product Features

**Document ID:** DOCSFLIP-FEA-001  
**Title:** Product Features  
**Version:** 0.1 (Draft)  
**Status:** Active Draft  
**Repository Path:** `docs/03-product/`  
**Authority:** Founder  
**Parent Documents:** DOCSFLIP-JNY-001

---

# 1. Purpose

This document defines the product capabilities required to deliver the user journeys established in JNY-001. It serves as the bridge between user experience and detailed product requirements.

---

# 2. Feature Design Principles

- Every feature must support one or more user journeys.
- Features describe capabilities, not implementation.
- Features should be independently understandable.
- Commercial behaviour is defined in COM-001.

---

# 3. Feature Domains

## A. Account & Identity
- User registration
- Authentication
- Profiles
- Password recovery

## B. Organisation Management
- Organisation workspaces
- Team invitations
- Roles & permissions

## C. Publishing
- PDF upload
- Conversion
- Publication preview
- Publish workflow

## D. Commercial
- Wallet
- Credits
- Transactions
- Purchase history

## E. Publication Management
- Publication library
- Updates
- Archive
- Renewals

## F. Distribution
- Share links
- QR codes
- Embeds

## G. Analytics
- Publication metrics
- Reader engagement
- Usage summaries

## H. Administration
- User administration
- Organisation administration
- Platform operations

---

# 4. Journey Traceability

| Journey | Feature Domains |
|----------|-----------------|
| Discover | A |
| Register | A |
| Create Organisation | B |
| Upload | C |
| Preview | C |
| Acquire Capacity | D |
| Publish | C, D |
| Share | F |
| Manage | E |
| Review Insights | G |

---

# 5. Outputs

The capabilities in this document are decomposed into functional and non-functional requirements within REQ-001.

---

# 6. Foundational Decisions

1. Every feature traces to a user journey.
2. Every requirement traces to one or more features.
3. Features remain technology-independent.
