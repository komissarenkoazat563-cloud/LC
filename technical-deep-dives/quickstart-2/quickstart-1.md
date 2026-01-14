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

Coupons and discounts are not just “codes.” They are active promises. Customers receive them in email, see them in ads, and expect them to work at checkout.

After shopping cart migration, the most damaging promotion failure is not missing coupon data. It is a customer entering a valid code and seeing “invalid” or getting a different outcome than expected.

#### Why promotions become risky during migration

Promotions are rule systems. Carts can differ in:

* How discounts apply (per order vs per item)
* Whether multiple discounts can stack
* Minimum purchase thresholds and usage limits
* Expiry logic and interpretation
* How free shipping or shipping discounts are represented

This can create a mismatch where a promotion exists but behaves differently.

#### What “promotion continuity” should mean

For most stores, the best continuity goal is:

* Your most important active promotions still work on the new cart
* The customer experience at checkout matches expectations for those promotions
* Your team has a plan to rebuild or simplify legacy promotions that do not translate cleanly

You do not need every expired or unused promotion to carry forward. You do need confidence that your current marketing promises will not break.

#### A practical planning approach

Start with a short list:

* Top active promo codes currently driving revenue
* “Always-on” offers (welcome code, free shipping threshold, VIP offers)
* Promotions used in scheduled campaigns in the next 30 to 60 days

Then decide what to do with long tail promos:

* retire them
* rebuild selectively
* treat them as a clean-up opportunity

#### How Next-Cart reduces promotion disruption

Promotion continuity is easier when you validate outcomes, not only data presence.

What Next-Cart does:

* Helps you identify which promo rules are critical to preserve
* Supports a Demo Migration so you can review representative promotions and expected outcomes early
* Helps you detect when rule behavior differences may require a higher-touch approach
* If you need selective migration or cleanup logic, this is a common reason to use Custom Migration with Custom Jobs

**Outcome:** your store launches with core promotions working as customers expect, reducing lost sales and support tickets.

#### Conclusion

Promotion failures are conversion failures. Treat coupons and discounts as part of your migration readiness checklist, validate what matters most, and plan cleanup intentionally.

**One next step (CTA):** If promotions play a major role in your revenue, validate your top active promo rules through a **Demo Migration** review so you can confirm continuity before go-live.

#### FAQs

<details>

<summary><strong>Why do coupons stop working after migration even if they exist?</strong></summary>

Because carts can interpret the rules differently. The code may exist, but thresholds, stacking, or application logic can change.

</details>

<details>

<summary><strong>Should I migrate every coupon ever created?</strong></summary>

Usually no. Most stores benefit from migrating only active or strategically important promotions and treating the long tail as cleanup.

</details>

<details>

<summary><strong>How does Next-Cart support coupon continuity?</strong></summary>

By helping you define critical promotions, validating representative outcomes early, and utilizing **Custom Migration** when you need selective migration or rule-specific handling.

</details>
