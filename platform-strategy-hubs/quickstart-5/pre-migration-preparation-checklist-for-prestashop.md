# Pre-migration Preparation Checklist for PrestaShop

A PrestaShop migration rarely fails because data cannot be transferred. It fails when the store’s logic is recreated differently on the new platform, often without anyone noticing until customers start browsing, filtering, or checking out.

PrestaShop is especially sensitive to this because day-to-day store behavior is shaped by how you model variations (combinations), how you represent specifications (features), how you segment customers (groups), and how much of your business logic lives inside modules or customizations. If these decisions are not made intentionally before migration, the new store can look “complete” while still behaving incorrectly in the places that matter most.

Use this checklist as a planning gate before you commit to the final migration run. The objective is not documentation for its own sake. It is to define what “correct” means for your store in PrestaShop so your migration can be validated with confidence.

If you need deeper context on how PrestaShop structures products, customers, and operational logic, review **PrestaShop Data Model Differences** before you finalize this checklist.

#### 1) Inventory what is “platform-native” vs “module-owned”

PrestaShop stores often rely on modules to extend core behavior. Before migration, create a simple inventory of what your current store depends on so you can plan what must be recreated and what can be simplified.

Preparation checks:

* List modules that affect catalog structure, pricing, promotions, checkout, shipping, tax, SEO, and content.
* Identify any custom fields that exist only because of a module, an integration, or custom development.
* Flag modules that “change meaning” (for example, they alter product availability rules, pricing logic, or checkout behavior).
* Decide which behaviors must be preserved exactly vs which can be replaced with a simpler, PrestaShop-native approach.

Pass condition:

* You can explain which parts of your store are core and which parts are extensions, and you have agreed which ones are in scope for recreation.

#### 2) Define your variation logic using attributes and combinations

In PrestaShop, product variations are typically modeled through attributes and combinations. This is the foundation for how shoppers select options and how stock and pricing can differ across variants.

Preparation checks:

* Define which option sets must create sellable variants (for example: size, color, material).
* Confirm whether variant-level identifiers are required (SKU-like references per combination).
* Clarify which variants have unique images, prices, or stock.
* Identify products where the source platform treated variants as separate products and decide how to represent them in PrestaShop without breaking navigation or SEO intent.

Pass condition:

* You can describe, per product type, how customers will choose options and how those choices map to sellable variants in PrestaShop.

#### 3) Separate “features” from “variations” to protect filtering and merchandising

Many stores mix together two ideas:

* What a product is (specifications)
* What a product can be (variants)

PrestaShop supports both concepts, but they serve different outcomes. If you map them incorrectly, your store can lose filtering accuracy, comparison clarity, and category navigation quality.

Preparation checks:

* Identify specification-like fields that must remain consistent across all variants (for example: dimensions, technical standards, compatibility).
* Decide which specifications must be filterable, which must be displayed only, and which can be removed entirely.
* Confirm how specification values should appear in product presentation and in category-level filtering.

Pass condition:

* Each attribute or spec from the source store has an intentional destination: variation logic, filterable spec, display-only spec, or out-of-scope.

#### 4) Rebuild category navigation as customer journeys, not a folder structure

Categories in a successful store are not just organization. They are browsing paths. Your preparation should treat category structure as a shopper behavior model.

Preparation checks:

* Identify your highest-traffic categories and their expected product coverage.
* Document the intended browse path for key buyer journeys (how customers narrow from broad to specific).
* Identify “navigation categories” that exist only for merchandising, promotions, or grouping.
* Decide how to handle products that belong in multiple categories without confusing the “primary” browsing path.

Pass condition:

* Your category plan describes how customers should discover products, not just where products should be stored.

#### 5) Clarify segmentation and pricing rules before migrating customers

In PrestaShop, customer segmentation and pricing outcomes can be shaped by customer groups and pricing rules. If you migrate customers without defining how segmentation should behave, your store can appear correct while pricing or tax display behavior is wrong for important audiences.

Preparation checks:

* Identify customer segments that must keep distinct pricing or tax-display behavior (for example: B2B vs retail).
* Decide whether group membership needs to be migrated or rebuilt.
* Document any tiered pricing, catalog-level rules, or customer-specific pricing logic that must be preserved.
* Confirm whether coupon logic and promotion structure should be recreated exactly or simplified.

Pass condition:

* You can describe how a returning customer should be classified and what pricing they should see, without relying on manual intervention.

#### 6) Confirm localization scope (languages, currencies, and regional rules)

Internationalization can change the meaning of prices, content, and store policies. Confirm what is in scope before migration so your validation is not ambiguous.

Preparation checks:

* Confirm the languages that must be supported at launch.
* Confirm the currencies that must be supported at launch.
* Identify which product content fields must be localized vs which can remain in one language initially.
* Confirm regional differences that affect operations, such as tax expectations, shipping rules, or customer communications.

Pass condition:

* Your target store scope is explicit: which languages, which currencies, and what level of localization completeness is required for launch.

#### 7) Define shipping and tax expectations as operational outcomes

Shipping and tax configuration is not just “settings.” It determines whether checkout totals are correct, whether customers trust the store, and whether operations can fulfill orders consistently.

Preparation checks:

* Define the shipping logic that must be preserved (weight-based, price-based, destination-based, carrier-based).
* Identify products where shipping depends on special conditions (oversized, hazardous, fragile, free-shipping eligibility).
* Confirm the tax model expectations at a planning level (how tax rules are applied, and whether prices are shown tax-included or tax-excluded for key audiences).
* Decide which outcomes must be validated first (for example: correct totals for top-selling SKUs shipped to top destinations).

Pass condition:

* You can name the 5–10 highest-risk checkout scenarios and what “correct” looks like for each.

#### 8) Map order lifecycle meaning before migrating history

Order history is valuable only if it retains meaning. If you migrate orders without defining how statuses and transitions should be interpreted in PrestaShop, reporting and support workflows can break.

Preparation checks:

* Identify the order statuses that matter to your team and customers (paid, shipped, delivered, refunded, canceled).
* Decide how historical statuses should be mapped when the source platform has different definitions.
* Confirm whether invoices, shipments, or fulfillment information must be present for historical orders, or if it is acceptable to preserve only a simplified state.

Pass condition:

* A team member can review a migrated order and interpret it correctly without needing the old platform open.

#### 9) URL continuity and redirects

Not every migration needs a large redirect effort. If most of your acquisition is not SEO-driven, a smaller approach is often enough.

Preparation checks:

* Create a “priority URL list” (top categories, top products, top content pages, top inbound-link targets).
* Decide which URLs must be preserved exactly vs which can redirect to the closest equivalent destination.
* Define how you will validate URL behavior on the new site before go-live, using path-to-path checks on a staging domain.

Pass condition:

* You can test a small set of priority URLs end-to-end and confirm the destination behavior is acceptable.

#### 10) Build a Demo Migration sample that reflects real complexity

A Demo Migration is not a data transfer test. It is a store behavior test. Your sample must reflect the complexity that creates migration risk.

A strong sample typically includes:

* Best-selling products across key categories.
* Products with multiple combinations and option logic.
* Products where pricing, stock, or images differ by variant.
* Products affected by modules or custom fields.
* Customers from key segments (including B2B-like segments, if applicable).
* Orders that represent your most common checkout scenarios.

Pass condition:

* Your demo sample includes enough complexity that a successful result gives you confidence, not false comfort.

#### 11) Assign validation ownership and sign-off criteria before final migration

Validation fails most often because it is treated as a general review instead of an owned process.

Preparation checks:

* Assign owners for catalog integrity, customer behavior, operational integrity, and storefront experience.
* Define “pass criteria” for each area (what must be true for sign-off).
* Decide which issues require correction before launch vs which can be scheduled post-launch.

Pass condition:

* Validation has owners, criteria, and a decision mechanism, not just a checklist.

#### 12) Choose the migration approach based on evidence, not assumptions

Your Demo Migration results and preparation outcomes should drive the right service selection.

Practical guidance:

* If the demo results are clean and scope is standard, a streamlined approach may be sufficient.
* If modules, complex combinations, segmentation, or operational rules create uncertainty, a managed approach often reduces risk.
* If you require custom handling of fields, unique logic, or special workflows, plan for a custom scope.

Pass condition:

* Your migration approach is chosen because the demo and scope evidence support it.

#### Conclusion

A strong PrestaShop migration plan is built around behavior, not totals. When you define how products should be chosen, how specifications should be represented, how customers should be segmented, and how orders should retain meaning, you prevent the most common failure pattern: a store that looks correct but behaves incorrectly.

Treat this checklist as your pre-migration contract with your future store. If every pass condition is met, your migration becomes predictable, testable, and far easier to validate.

You can run a Demo Migration to validate the most important store behaviors before committing to the full migration. If you prefer an assisted approach, you can share a representative sample of your data, and Next-Cart can run the Demo Migration and provide the results for review. For scoping support or expectation alignment, Live Chat is the fastest way to confirm what should be preserved, what can be simplified, and which migration approach best fits your store.

#### FAQs

<details>

<summary><strong>Is it possible to migrate to a localhost website?</strong></summary>

Migration tools typically require a publicly reachable website URL to connect and transfer data. If you want a private environment for testing, use a staging site with controlled access rather than a local-only address.

Or you can setup a temporary public URL for localhost using [Ngrok](https://ngrok.com/download). After installing Ngrok and starting a tunnel, you will get a public URL for your localhost site. You can enter the URL in the migration tool and start the migration.

</details>

<details>

<summary><strong>What should I include in a high-quality demo sample for PrestaShop?</strong></summary>

Your best sellers, your most combination-heavy products, and the categories that drive the most revenue. The goal is validating outcomes, not just counts.

</details>

<details>

<summary><strong>How does URL Redirect work?</strong></summary>

URL redirects are used to send visitors from old URLs to the correct new destination after a migration. The practical planning step is to prioritize the URLs that matter most (top products, top categories, key landing pages) and validate that those URLs resolve correctly before launch.

</details>

<details>

<summary><strong>Can I migrate new orders and other data after finishing the first migration process?</strong></summary>

Yes. If new records are created after your initial migration, you can use Recent Data Migration to bring over the new data without repeating the full migration.

</details>
