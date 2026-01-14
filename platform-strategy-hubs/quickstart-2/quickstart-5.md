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

# WooCommerce Validation Priorities:

WooCommerce validation should be behavior-first. Because themes and plugins influence how data is presented, validation must confirm customer and operator outcomes, not just migrated totals.

#### Priority 1: Variation integrity and purchase behavior

Validate:

* Variants are selectable and purchasable as expected
* Option naming is consistent
* Pricing, stock, and SKU behavior matches expectations

#### Priority 2: Category browsing and product discoverability

Validate:

* Category assignment matches merchandising intent
* Filtering and sorting behavior works for key collections

#### Priority 3: Custom field visibility

Validate:

* Meaning-critical custom fields appear where shoppers and staff rely on them
* Feeds and integrations receive the fields they require

#### Priority 4: Order usability and historical order continuity

If order history is in scope:

* Validate representative order types and workflows
* Consider target order storage mode because WooCommerce may use HPOS order tables on new installs.

#### Priority 5: URL continuity and redirects

Validate:

* Priority URLs resolve correctly after launch
* Redirect strategy exists when permalink structure changes, since redirects in WordPress are commonly handled via plugins or server rules.\
  WooCommerce permalinks include configurable product and category bases.

#### Conclusion

WooCommerce validation succeeds when it targets the exact places variability shows up: variations, custom fields, plugin-driven behaviors, and SEO continuity.

If you want high confidence without validating everything at once, use a **Demo Migration** sample and validate only the top behaviors: complex variations, top categories, critical custom fields, and priority URLs.
