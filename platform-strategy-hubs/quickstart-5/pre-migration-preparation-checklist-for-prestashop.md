# Pre-migration Preparation Checklist for PrestaShop

PrestaShop preparation is mostly about identifying where meaning lives: combinations, module behavior, multistore scope, and URL expectations.

#### 1) Module and integration inventory

List modules that affect:

* Pricing and promotions
* Checkout and payment flows
* Product customization or variant logic
* SEO and URL behavior

Goal: identify which modules define revenue-critical behavior.

#### 2) Combination audit for catalog risk

Identify:

* Products with many combinations
* Attribute groups with inconsistent naming or values
* Products where variation selection is tied to pricing or images

Goal: define what must remain true in purchase behavior.

#### 3) Multistore scope plan

If multistore is involved, define:

* What is shared across stores (catalog, customers, pricing)
* What differs by store (domains, pricing strategies, content)

PrestaShop multistore exists to manage several front offices from one back office, but that flexibility must be planned.

#### 4) URL continuity priorities

List:

* Highest traffic product and category URLs
* Landing pages that drive paid or organic traffic
* URLs that must remain stable

PrestaShop has canonical URL settings and friendly URL behavior that should be validated early.

#### 5) Define a validation sample

A strong sample includes:

* Best sellers with many combinations
* Products that rely on module-driven behavior
* Top categories that drive navigation
* SEO-critical URLs

**Next-Cart insight**: A Demo Migration turns this checklist into evidence by showing how your real products and relationships appear in the target environment, before full scope is purchased.

If you are unsure what to prioritize, reach out via **Live Chat** and **Next-Cart** will perform a Demo Migration on your sample with complex products and SEO-critical URLs first, then finalize the project plan around what the results reveal.
