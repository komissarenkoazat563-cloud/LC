---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
metaLinks:
  alternates:
    - /broken/spaces/EwOn3si2UOVRL65zVOMg/pages/1gn4Fc2mLPsjb0Ss3GKj
---

# Promotions and Coupons: Rule Differences Across Platforms

Promotions drive conversion, but promotions are rarely portable in a clean “copy and paste” way. Even when a coupon code name transfers, the behavior behind it can change because platforms apply discounts differently, enforce different eligibility rules, and calculate totals in different layers.

This article explains why promotions and coupons often behave differently after a shopping cart migration, what typically changes, and how to validate the discount scenarios that matter most before go-live.

### Why promotions behave differently after migration

Promotions are not just data. They are **rules** that interact with cart structure, product eligibility, customer segmentation, and tax/shipping logic. When the platform changes, one or more of these elements can change too.

Common sources of differences include:

* different promotion engines and rule models
* different ways discounts are stored (order-level vs line-level)
* different stacking rules and exclusions
* different treatment of shipping discounts
* different rounding and calculation order that affects totals

**Planning mindset**: you are preserving **discount intent**, not only transferring coupon codes.

### Core concept 1: Coupons vs promotions are not the same thing

#### Coupon code

A code a customer enters (or a link applies) to trigger a discount.

#### Promotion rule

The logic that defines what the discount does: eligibility, exclusions, limits, thresholds, stacking behavior, and how the discount is applied across items.

A coupon can migrate in name and still fail in behavior if the rule logic cannot be represented the same way on the target platform.

### Core concept 2: Discounts can be applied at different layers

Platforms commonly represent discounts in different layers:

#### Order-level discount

A single discount applied to the total order amount.

#### Line-item discount

Discounts applied directly to individual products or quantities.

#### Shipping discount

Discounts applied to shipping cost (free shipping or reduced shipping), often with its own eligibility conditions.

These differences matter because they change how:

* totals are displayed to customers
* historical orders appear
* support teams interpret what happened
* taxes interact with discounted amounts

### Core concept 3: Eligibility and stacking rules vary widely

Promotions often include conditions such as:

* minimum spend thresholds
* specific product or category eligibility
* customer segment eligibility
* exclusions (sale items, gift cards, certain collections)
* limits (one-time use, per-customer limits)
* stacking behavior (can it combine with other discounts?)

Even when two platforms support “the same” concept, the details can differ. The risk is that a promotion that drives a meaningful share of revenue stops behaving predictably after migration.

Expert insight: discount problems rarely show up in the simplest cart. They show up in the cart that actually reflects your business: mixed eligibility, thresholds, and stacked behaviors.

### The most common pitfalls during migration

#### Recreating promotions late

Teams often rebuild discounts at the end because they are “marketing tasks.” That is when mistakes are hardest to catch and most expensive to fix.

#### Validating only one or two basic coupons

A coupon that works on a single item cart may still fail in real scenarios, especially when thresholds, exclusions, or stacked discounts are involved.

#### Assuming “the total is right” means the promotion is right

Totals can appear correct while the discount distribution changes in ways that affect margins, reporting, customer perception, or tax interactions.

#### Ignoring shipping promotions

Free shipping and shipping thresholds are common drivers of conversion. These are often treated differently across platforms and deserve explicit validation.

### How to scope promotions without rebuilding everything at once

Instead of trying to recreate every historical promotion, start with a priority set:

#### Priority promotion set (recommended)

* your most-used coupon codes
* your highest-revenue promotions
* your most common threshold discounts (spend X get Y)
* your core shipping incentives (free shipping thresholds, shipping discounts)
* any promotion patterns that are “brand expectations” (welcome discount, VIP discount)

Then decide how to handle the long tail:

* recreate only active, meaningful promotions
* retire old codes that no longer serve a purpose
* consolidate multiple similar discounts into a smaller set of cleaner rules

This is usually more effective than rebuilding everything and hoping it matches.

### What to validate before go-live

Validate promotion behavior through representative carts, not through rule screens.

#### Build a test set of carts that includes

* single-item and multi-item carts
* mixed eligibility carts (eligible and ineligible items)
* threshold carts near the boundary (just under and just over)
* shipping incentive scenarios (free shipping thresholds)
* high-impact customer segments if you use segmented pricing or discounts

#### Validate outcomes that matter

* the discount applies to the intended items
* exclusions behave as expected
* stacking behavior matches your rules
* totals are credible and explainable to customers
* the promotion does not create unexpected margin loss

### How Next-Cart helps reduce promotion-related launch risk

Next-Cart helps teams avoid revenue-impacting surprises by treating promotions as a validation and expectation-alignment topic, not a last-minute rebuild task.

Support often includes:

* helping you identify which promotions are truly high impact
* translating discount intent into a priority scenario test set
* flagging where platform rule models may require a simplified or adjusted approach

The goal is predictable checkout behavior and fewer post-launch “why didn’t my discount work” tickets.

### Conclusion

A practical industry takeaway is that promotions break during migration because platforms do not just store coupons. They interpret them. When discount intent is not translated into equivalent rule behavior and validated with real carts, the launch risk shows up immediately as conversion loss, margin surprises, or support spikes. If you prioritize your highest-impact promotions, validate the scenarios customers actually use, and treat promo behavior as a go-live requirement, you protect revenue continuity more reliably than by trying to recreate everything.

If discounts and shipping incentives drive a meaningful share of your conversions, define a “priority promotion set” and validate it using real cart scenarios before go-live. If you want help identifying which coupon rules are most likely to behave differently on your target platform and building a high-signal validation set, reach out via Live Chat. Next-Cart can help you align promotion intent with practical platform behavior and choose the safest service approach for protecting promo-driven revenue during migration.

#### FAQs

<details>

<summary><strong>Why do coupon rules change after migrating to a new platform?</strong></summary>

Because platforms apply discounts using different rule models, stacking behavior, and discount layers (order-level, line-level, shipping). Even when a coupon code name transfers, the underlying behavior may not match unless it is recreated and validated.

</details>

<details>

<summary><strong>Can I migrate only valid or unused coupons?</strong></summary>

In some cases, coupon scope can be filtered, but “valid,” “unused,” and “active” can mean different things depending on how the source platform tracks coupon rules and history. If coupon selection criteria matter, define the rule clearly and validate it against real promotion scenarios.

To implement a data filter for migration, you will typically need to leverage a Custom Migration Service. This model will enable you to apply a specific filter to exclude any data you don't need to migrate.

</details>

<details>

<summary><strong>Why do coupons stop working after migration even if they exist?</strong></summary>

Because carts can interpret the rules differently. The code may exist, but thresholds, stacking, or application logic can change.

</details>

<details>

<summary><strong>Should I migrate every coupon ever created?</strong></summary>

Usually no. Most stores benefit from migrating only active or strategically important promotions and treating the long tail as cleanup.

</details>

<details>

<summary><strong>What should I validate first for promotions after migration?</strong></summary>

Validate your highest-impact promotions using representative carts: threshold discounts, shipping incentives, and your most-used coupon codes. Focus on eligibility, exclusions, stacking, and whether the outcome is explainable to customers and support.

</details>
