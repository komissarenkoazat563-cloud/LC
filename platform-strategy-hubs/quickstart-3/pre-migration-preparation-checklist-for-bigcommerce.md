# Pre-migration Preparation Checklist for BigCommerce

Preparation for BigCommerce is mostly about clarity: what becomes a variant, what becomes a modifier, how browsing is structured, and what custom data must remain usable.

#### 1) Catalog complexity audit

**Identify**:

* Products with many combinations
* Products that mix true variants with personalization
* Options that have unusually large value lists

**Reason**: BigCommerce distinguishes variants from modifiers, and modifiers do not generate inventory-tracked combinations.

#### 2) Variant vs modifier classification plan

**Define**:

* Which choices must be inventory-tracked variants
* Which choices are customizations best handled as modifiers

#### 3) Category and category tree strategy

If you have multiple storefronts or channels, decide what each should show and how category trees should represent that.

Also confirm category assignment discipline, since products can belong to many categories but with a published cap of 1,000.

#### 4) Custom data inventory

List custom fields and attributes that matter to:

* Product pages
* Filtering and search
* Feeds and integrations

BigCommerce supports product custom fields and broader metafields that can be stored across objects.

#### 5) Integration inventory and timing realism

List systems that touch the catalog or orders. If the integrations run alongside the migration, API rate limits can influence throughput and sequencing.

#### 6) Validation sample definition

A good BigCommerce sample includes:

* Best sellers
* Most complex configurable products
* A few critical categories per storefront channel
* A set of SEO-critical URLs and redirect expectations

#### Next-Cart insight: turning preparation into proof

Many teams struggle to translate preparation checklists into confidence. A Demo Migration converts the checklist into evidence by letting you review how real products, variants, category assignments, and key attributes appear on BigCommerce.

If you are still unsure which products should use modifiers vs variants, feel free to reach out for expert support and consultation via **Live Chat**.

Or you can request Next Cart run a **Demo Migration** with your most configurable products first and use the output to finalize the scope, for free.
