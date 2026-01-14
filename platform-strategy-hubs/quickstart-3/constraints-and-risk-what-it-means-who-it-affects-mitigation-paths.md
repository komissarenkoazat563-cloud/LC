# Constraints and Risk: What It Means, Who It Affects, Mitigation Paths

Constraints are not automatic blockers. They are planning inputs. The goal is to define:

* What the constraint means
* Who it affects
* The mitigation paths that keep quality intact

#### Constraint 1: Variant SKU ceiling per product

**What it means:** BigCommerce references support for complex catalogs up to **600 SKUs per product**.

**Who it affects:** configurable products with many combinations

**Mitigation paths:**

* Convert optional personalization to modifiers instead of variants when inventory tracking is not required.
* Split products strategically when a single listing would exceed SKU limits
* Validate complex products first, not last

#### Constraint 2: Option value ceiling

**What it means:** BigCommerce caps **option values per option at 250**.

**Who it affects:** long pick lists, highly configurable options

**Mitigation paths:**

* Consolidate values where possible
* Reframe extreme lists into modifiers or structured custom fields where suitable

#### Constraint 3: Categories per product limit

**What it means:** BigCommerce caps categories per product at **1,000**.

**Who it affects:** stores that use categories as tags, or deeply multi-assigned products

**Mitigation paths:**

* Redesign classification strategy, using categories for navigation and other attributes for filtering

#### Constraint 4: Multi-storefront and category tree complexity

**What it means:** BigCommerce uses category trees and you can assign multiple trees to storefront channels.

**Who it affects:** multi-brand, multi-region, or multi-channel catalogs

**Mitigation paths:**

* Define the target browsing experience per storefront channel
* Validate each channel’s critical browse paths separately

#### Constraint 5: API rate limits (integration and migration throughput)

**What it means:** BigCommerce enforces API rate limits that vary by plan, refreshed on intervals such as 30 seconds, with published quotas by plan tiers.

**Who it affects:** very large catalogs, heavy integration environments, tight timelines

**Mitigation paths:**

* Plan migration windows realistically for large stores
* Avoid compressing validation into the final week

#### Constraint 6: Redirect management

**What it means:** BigCommerce supports 301 redirects with dedicated management endpoints.

**Who it affects:** SEO-sensitive stores and stores changing URL structures

**Mitigation paths:**

* Build a prioritized URL mapping plan early
* Validate top traffic URLs before launch

#### Conclusion

BigCommerce constraints are manageable when you plan around catalog structure, variants vs modifiers, and throughput realities.

If two or more constraints apply to your store, reach out via **Live Chat** to request **Next-Cart** run a **Demo Migration** for you on complex products and top categories first, then select Standard, Managed, or Custom based on what the demo reveals.
