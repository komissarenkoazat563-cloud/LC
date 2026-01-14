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
---

# PrestaShop Data Model Differences: What Changes and Why It Matters

PrestaShop migrations are primarily about preserving meaning. In PrestaShop, meaning often depends on:

* How products are modeled with combinations
* How attributes and features are used
* How categories support navigation
* How multistore scope changes what “the same product” means
* How SEO settings influence URL behavior

#### Products and combinations

PrestaShop uses the term **combinations** to describe product variations created by combining attributes.

Why it matters:

* If your source platform models variants differently, mapping needs to preserve purchasable choices and inventory behavior.
* Combination-heavy catalogs increase validation effort because small attribute issues can cascade into many variation outcomes.

#### Attributes vs features

PrestaShop distinguishes customer-selectable attributes (used to build combinations) from non-selectable descriptive data, often represented as features.

Why it matters:

* Some source platforms store everything as attributes even when customers never select it.
* Migration planning should decide what must drive selection versus what should remain descriptive.

#### Categories and navigation

PrestaShop catalogs rely on categories to create browse structure. The migration risk is not that categories migrate, but that the browsing experience changes if category strategy shifts.

Why it matters:

* If customers rely on category paths to find products, category integrity becomes a top validation priority.

#### Multistore scope

PrestaShop’s multistore feature allows managing several front offices from a single back office, including cases with different domains, branding, or pricing per store.

Why it matters:

* A migration must define where data is shared versus store-specific.
* Validation must be done per storefront context when behavior differs.

#### SEO and URL behavior

PrestaShop supports friendly URLs when the server supports URL rewriting and includes canonical URL settings with 301 or 302 behavior based on launch stage.

Why it matters:

* URL continuity is not just a technical detail, it directly affects traffic and trust.
* PrestaShop SEO outcomes are influenced by configuration, server behavior, and sometimes modules.

#### Conclusion

PrestaShop’s model supports flexible catalogs and multistore, but migration quality depends on mapping combinations correctly, planning multistore scope, and treating URL behavior as a first-class deliverable.

If your catalog uses many combinations or your store runs multistore, use a **Demo Migration** to validate how variations and store contexts translate before locking full scope.
