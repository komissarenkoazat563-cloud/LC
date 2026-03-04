# Pre-migration Preparation Checklist for Square

OpenCart migrations go sideways less because “data didn’t move” and more because store behavior quietly changes. Products import, customers import, orders import, but the buying and browsing experience shifts: option selection behaves differently, filtering stops reflecting real intent, multi-store scope blurs, or SEO keyword URLs do not resolve the way search engines and shoppers expect.

OpenCart is a lean, extensible platform. That is an advantage, but it also means your store’s meaning is often distributed across extensions, configuration, and the way you model options, attributes, filters, and store assignments. Preparation is how you make that meaning explicit before you commit to full execution.

### What “good preparation” means for OpenCart

Good OpenCart preparation means you can answer these questions clearly:

* Which extensions and customizations define what customers can buy and how totals are calculated?
* Which product selections must remain true in the target (options, pricing adjustments, availability rules)?
* Which attributes and filters must remain usable for discovery (category browsing, narrowing, search intent)?
* Are you migrating into a single store or an OpenCart multi-store structure, and what differs by store?
* What does “success” look like for order usability (statuses, totals breakdown, refunds) and for SEO continuity (priority URLs)?
* What does your target environment need to be true for (OpenCart version fit, hosting requirements, extension compatibility, SEO keyword URL behavior)?

If you cannot answer these yet, that is normal. The purpose of the checklist is to help you build those answers early, using a Demo Migration sample that reveals real risk.

### OpenCart Preparation Checklist

#### 1) Build a representative Demo Migration sample

Choose a sample designed to expose complexity, not to “look clean” in reporting.

Include:

* Best sellers with the most complex option combinations (example: size + color where each choice changes price or availability)
* Products that rely on attributes for merchandising or comparisons
* Categories where filters matter to conversion (the pages where shoppers narrow down, not just browse)
* Products that represent edge cases (unusual pricing logic, unusual inventory patterns, file upload options if you use them)
* A few representative customer profiles (guest-like patterns vs registered buyers, and any segmentation you use)
* A small set of operational order scenarios (discount-heavy orders, shipping-heavy orders, refunds if common)
* Priority URLs (top organic landing pages, top revenue products, key categories, campaign landing paths)

Goal: reveal what needs mapping decisions, what is a platform difference, and what may require Custom Jobs, before full scope is locked.

#### 2) Inventory extensions and classify what they control

OpenCart stores often “work” because extensions are defining outcomes. List extensions and group them:

* Revenue-critical (must preserve customer-facing outcomes)
* Operations-critical (must preserve workflows for support, fulfillment, reporting)
* Optional (nice-to-have)

For each revenue/ops-critical extension, document:

* Which entity it affects (Product, Customer, Order, SEO)
* Which outcome it must preserve (plain-language “must remain true” statements)

Examples of outcome statements:

* “Wholesale customers must see different pricing.”
* “A selected option must adjust the final price.”
* “The totals breakdown must remain interpretable for accounting.”

#### 3) Normalize product option and attribute structure before you map

OpenCart’s catalog behavior depends heavily on how consistently you structure options and attributes.

Preparation actions:

* Standardize option names and value formats across the catalog (avoid five spellings for the same concept)
* Identify products where the same attribute is represented differently (free-text on some items, structured on others)
* Identify where option selection changes price, availability, or fulfillment handling
* Document any non-standard option logic controlled by extensions

Validation gate:

* For your demo sample, write “buying path pass conditions” for option selection (selection → price display → add-to-cart → checkout outcome).

#### 4) Treat filters as “discovery infrastructure,” not a cosmetic feature

If your store depends on filtering to help customers find the right subset of products, plan it as meaning preservation, not UI polish.

Preparation actions:

* Identify which categories rely on filters to convert
* List the filter groups and attribute concepts that must remain usable
* Confirm which product attributes are informational vs discovery-driving
* Decide how you will validate discovery quality (can shoppers reproduce the same narrowing paths that exist today?)

One-sentence recap link: For deeper planning on how OpenCart options, attributes, filters, and store assignment shape post-migration behavior, review OpenCart Data Model Differences.

#### 5) Define your OpenCart store structure early (single store vs multi-store)

OpenCart supports multi-store under one installation, but migration scoping depends on what differs by store.

Preparation actions:

* Decide whether you are migrating into one store or multiple storefronts
* Document what differs by store (catalog assignment, pricing, languages, currencies, content pages, shipping/payment rules)
* Identify records that belong to specific stores and must not “leak” into other storefronts
* Include at least one store-specific slice in your Demo Migration sample if multi-store is in scope

Validation gate:

* Confirm store assignment logic produces the expected storefront experience for representative products and categories.

#### 6) Clarify customer account expectations and login continuity plan

Customer and account data can migrate successfully while customer experience still degrades if expectations are not set correctly.

Preparation actions:

* Identify customer groups/tiers that drive behavior (pricing access, approvals, tax handling, B2B rules)
* Decide what customer history is operationally necessary versus optional
* Plan the post-migration login experience (what you want returning customers to experience on first login)

Password continuity planning:

* If both source and target are open-source and password hashes can be transferred, customer password continuity may be possible using the Next-Cart Customer Password Plugin (compatible targets include OpenCart).
* If that is not applicable, plan a first-login password reset journey and validate it end-to-end before launch (reset email deliverability, account access, and a clear customer message).

#### 7) Define order history usability, not just order record completeness

OpenCart order usability depends on whether statuses and totals remain interpretable for the people who run the business.

Preparation actions:

* List the order statuses your team actually uses and what each status means operationally
* Identify the “must remain usable” fields for support and fulfillment (customer linkage, items, totals components, shipping and tax interpretation)
* Identify extensions that affect totals and operational interpretation (discount logic, shipping calculations, payment fees, store credit, reward handling)

Validation gate:

* For your demo sample, define “support workflow pass conditions” (a support rep can answer common questions from migrated orders without guessing).

#### 8) Decide URL continuity rules early and validate priority paths first

SEO continuity is a prioritization problem before it is an implementation problem.

Preparation actions:

* Build a prioritized list of critical URLs (top revenue products, top organic landing pages, key categories, high-intent content paths)
* Decide what should stay the same versus what can change in the destination URL pattern
* Confirm how you will maintain reachability of priority paths after launch (301 redirect strategy, canonical expectations, and a clear testing plan)

### Conclusion

OpenCart preparation is the process of making store meaning explicit: which extensions define outcomes, which option and attribute structures drive buying decisions, which filters represent discovery intent, and which store assignments define the customer experience across storefronts. When you standardize the catalog concepts that matter, scope multi-store correctly, and write pass conditions for option selection, discovery paths, order usability, and priority URL reachability, you reduce the most common risk: a store that looks migrated but behaves differently.

You can reduce uncertainty quickly by running a Demo Migration with a representative sample, then reviewing results to confirm what migrates cleanly versus what needs Custom Jobs or deeper execution support. If you prefer, you can provide sample data and ask Next-Cart to run the Demo Migration and share findings, then use Live Chat to align scope and choose the safest service model for your OpenCart target.

#### FAQs

<details>

<summary><strong>Do you support OpenCart multi-store migrations?</strong></summary>

Yes. Next-Cart supports OpenCart multi-store. The key planning step is scope: define whether you are migrating into a single store or a multi-store setup, what differs by store, and which records must remain store-specific. Your Demo Migration sample should include at least one store-specific slice so you can validate store assignment behavior before full execution.

</details>

<details>

<summary><strong>Do I need to keep the KitConnect package in my store after the migration?</strong></summary>

No. KitConnect is used as a bridge to connect the migration tool to a self-hosted store for data access. Once migration is complete, it typically does not need to remain in your store.

</details>

<details>

<summary><strong>How are product options, attributes, and filters handled when migrating into OpenCart?</strong></summary>

In OpenCart, product options are customer-facing selections made before adding to cart, while attributes typically support information and structured comparisons. Filters are commonly used to support category-page narrowing and discovery when your storefront is configured to display them. For migration planning, treat options as conversion-critical behavior, and treat filters and attributes as discovery infrastructure. Validate with real browsing paths, not just product counts.

</details>

<details>

<summary><strong>We use third-party extensions and custom fields on the source store. Can that data be migrated into OpenCart?</strong></summary>

Core platform data typically migrates well when it maps cleanly to OpenCart’s native model. Extension-managed data and custom fields often require explicit mapping work to remain usable, especially when those fields drive pricing, merchandising, or operations.

</details>

