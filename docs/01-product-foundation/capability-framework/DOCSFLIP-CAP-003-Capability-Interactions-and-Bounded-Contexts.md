# DOCSFLIP-CAP-003 --- Capability Interactions & Bounded Contexts

**Version:** 0.1 (Founder Draft)\
**Repository Path:** `docs/01-product-foundation/`

## Purpose

Define the interaction boundaries between the core business capabilities
and establish the bounded contexts that guide Product Architecture, Data
Architecture and Solution Architecture.

## Interaction Principles

-   Identity authenticates people.
-   Organisations own publications.
-   Publications are the central business asset.
-   Reader Experience consumes publications.
-   Commercial monetises publications.
-   Analytics measures outcomes.

## Bounded Contexts

  -----------------------------------------------------------------------
  Context                                    Owns
  ------------------------------------------ ----------------------------
  Identity                                   Users, credentials, profiles

  Organisations                              Organisations, workspaces,
                                             memberships

  Publications                               Publication lifecycle,
                                             hosting responsibility,
                                             metadata

  Reader Experience                          Reading interactions and
                                             preferences

  Commercial                                 Wallets, credits, payments,
                                             entitlements

  Analytics                                  Events, metrics, reporting
  -----------------------------------------------------------------------

## Shared Business Assets

  Asset             Authoritative Owner
  ----------------- ---------------------
  User              Identity
  Organisation      Organisations
  Publication       Publications
  Wallet            Commercial
  Analytics Event   Analytics

## Architectural Guidance

-   PA-001 elaborates these contexts.
-   DAT-001 allocates data ownership to these contexts.
-   ARC-001 defines technical implementation.
-   IMP-001 delivers the implementation.

## Constitutional Rule

Business responsibilities may cross capability boundaries through
collaboration, but ownership of a business asset shall belong to one
capability only.
