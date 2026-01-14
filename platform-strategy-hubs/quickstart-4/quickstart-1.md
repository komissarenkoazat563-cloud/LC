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
    - https://app.gitbook.com/s/EwOn3si2UOVRL65zVOMg/troubleshoot/quickstart-1
---

# Magento Data Model Differences: What Changes and Why It Matters

Magento migrations succeed when you preserve meaning, not just records. In Magento, meaning is often defined by:

* Product types and their relationships
* Attributes and attribute sets
* Store scope and multi-store structure
* SEO continuity through rewrites and redirects

#### Product types and catalog behavior

Magento supports multiple product types such as simple, configurable, virtual, downloadable, bundle, and grouped.

Why it matters:

* Product type affects how customers choose options, how inventory is tracked, and how products are presented.
* If your source platform models kits, bundles, or variations differently, mapping choices affect customer experience.

#### Attributes and attribute sets

Magento relies heavily on attributes, organized into attribute sets that act like templates for product records.

Magento’s EAV module exists to make entities configurable and extendable.

Why it matters:

* Attributes are not only product descriptions. They often drive filtering, layered navigation, promotions, comparisons, and discoverability.
* Attribute sprawl is common. Migration planning must decide which attributes are essential, which are redundant, and which must be standardized to support storefront behavior.

#### Multi-store, websites, stores, and store views

Magento installations have a hierarchy of websites, stores, and store views that controls scope.

Why it matters:

* A single installation can serve multiple storefronts with different root categories and sometimes different base URLs.
* Migration mapping must account for where catalog entities apply in that hierarchy.

#### SEO continuity through URL rewrites and redirects

Magento has a URL rewrites tool that creates permanent redirects (301) to preserve SEO value when URLs change.

Why it matters:

* URL continuity is a planning deliverable, not a post-launch detail.
* If your current store has deeply indexed URLs, redirect planning should start early.

#### Search requirements and implications

As of Adobe Commerce 2.4, installations must be configured to use Elasticsearch or OpenSearch for catalog search.

Why it matters:

* Search and filtering outcomes depend on attribute quality and platform configuration.
* This is one reason early validation should include filtering and search behavior, not just product pages.

#### Conclusion

Magento’s strength is flexibility. Migration quality depends on deliberate mapping of product types, attributes, and store scope, plus early SEO and search validation.

If your store relies on attribute-driven filtering or multiple storefronts, use a **Demo Migration** to validate attribute mapping and store scope outcomes before locking full migration scope.
