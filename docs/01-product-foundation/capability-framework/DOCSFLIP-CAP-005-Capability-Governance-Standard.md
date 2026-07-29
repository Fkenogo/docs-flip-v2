# DOCSFLIP-CAP-005 --- Capability Governance Standard

**Version:** 0.1 (Founder Draft)\
**Repository Path:** `docs/01-product-foundation/capability-framework/`

# Purpose

Define the governance rules for creating, modifying and retiring
business capabilities.

# Governance Principles

1.  Capabilities represent enduring business responsibilities.
2.  Capabilities are technology independent.
3.  Product Architecture expands capabilities but does not redefine
    them.
4.  Solution Architecture implements capabilities but does not own them.

# Introducing a New Capability

A new Level 1 capability shall only be approved if it:

-   Represents a distinct enduring business responsibility.
-   Owns one or more unique business assets.
-   Cannot reasonably be absorbed into an existing capability.
-   Has documented downstream impacts.
-   Receives explicit Founder approval.

# Modifying a Capability

Changes shall assess:

-   Business responsibility
-   Asset ownership
-   Downstream document impact
-   Backward compatibility
-   Founder approval requirement

# Retiring a Capability

A capability may only be retired after:

-   Responsibilities are reassigned.
-   Asset ownership is transferred.
-   Traceability is updated.
-   Founder approval is recorded.

# Relationship to Other Documents

-   CON-001 defines the product.
-   CAP-001--CAP-004 define the capability constitution.
-   PA-001 elaborates capability architecture.
-   ARC-001 implements the architecture.
-   IMP-001 delivers the implementation.

# Constitutional Rule

No downstream document may redefine the canonical capability model
established by CAP-001 without an approved Founder constitutional
decision.
