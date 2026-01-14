# Preserving Product Reviews and Ratings

Reviews and ratings are earned trust. During data migration, reviews are often at risk because they frequently live in third-party systems rather than the core cart database.

This article will explain why reviews are complicated, what continuity can look like, and how to plan for it without getting technical.

#### Why reviews matter during migration

Reviews influence:

* Conversion rates for high consideration products
* Perceived legitimacy for new visitors
* Customer confidence during a period of change

When a new site launches with missing reviews, the store can feel newer and less proven, even if everything else looks correct.

#### Why reviews create migration complexity

Reviews can involve:

* third-party apps or providers
* product linkage that must remain accurate
* moderation status, timestamps, and reviewer fields
* storefront display logic tied to the new theme or app configuration

Even when review data exists, the main risk is whether reviews remain attached to the correct products in the new store.

#### What continuity success looks like

For most stores, review continuity means:

* Reviews appear on the correct products
* Aggregate ratings are consistent for best sellers
* The product page still communicates trust clearly after migration

#### How to approach reviews in planning

Start by clarifying:

* where reviews currently live (native vs app-based)
* whether you need full review text or ratings only
* which products must retain reviews to protect conversion
* whether the target cart uses the same review system or a replacement

#### Validation guidance for reviews

Validate a small set first:

* best sellers
* products where reviews are a major conversion driver
* products with variants where linkage mistakes can happen

Check:

* reviews appear on the correct products
* ratings totals are plausible and consistent
* the storefront presentation supports trust (even if styling changes)

#### How Next-Cart helps preserve trust signals

Trust signals require explicit planning because they often depend on systems outside the cart.

What Next-Cart does:

* **Dependency discovery:** identifies where reviews live (native vs app-based) and what can be migrated
* **Relationship planning:** ensures review-to-product linkage is treated as a core requirement when applicable
* **Validation sample:** checks best sellers and high-consideration products first so trust signals are protected where they matter most
* **Service model guidance:** if reviews require custom handling, we recommend leveraging **Custom Migration** **Service** to achieve flawless results.

**Outcome**: You do not launch a “new-looking” store that lost its credibility.

#### Best practices

* Treat reviews as a separate workstream in migration planning.
* Identify your review system early and confirm what data is available.
* Decide the minimum acceptable continuity level before execution.
* Validate on the live customer experience, not just in a back-office list.

#### Common pitfalls

* Discovering late that reviews are stored in an app and were never included in scope
* Migrating reviews but losing the relationship to the correct products
* Launching with empty reviews on best sellers
* Treating review display as a theme issue only and missing data continuity requirements

#### Conclusion

If reviews influence conversion, they deserve first-class planning. Treat them as a trust deliverable, not an optional afterthought.

If reviews are critical to your conversion, use the **service model decision** logic to confirm whether your store needs Standard, Managed, or Custom migration support for trust-signal continuity.

#### FAQs

<details>

<summary><strong>Are reviews always part of a standard migration?</strong></summary>

Not always. Reviews often depend on third-party systems and may require additional planning or custom handling.

</details>

<details>

<summary><strong>What is the biggest review migration risk?</strong></summary>

Broken relationships. Reviews exist, but they appear on the wrong products or do not appear at all.

</details>

<details>

<summary><strong>Can I choose to migrate only ratings and not full review text?</strong></summary>

Sometimes. The right choice depends on your system and business goals. The key is to define the outcome you want before execution.

</details>

<details>

<summary><strong>When would I need Custom Migration for reviews?</strong></summary>

For custom requirements for the data being migrated, you may need to use the **Custom Migration** service

</details>
