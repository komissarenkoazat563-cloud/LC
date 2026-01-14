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
    - >-
      https://app.gitbook.com/s/EwOn3si2UOVRL65zVOMg/connection-guides/quickstart-3/quickstart-1
---

# WooCommerce Data Model Differences: What Changes and Why It Matters

WooCommerce is built on WordPress structures. That makes it highly extensible, but it also means data often lives across post types, taxonomies, and metadata, plus plugin-added fields.

This matters in shopping cart migration because meaning can be distributed across many places.

#### Products and variations

WooCommerce products and variations are stored in WordPress structures:

* Products and variations are stored in `wp_posts` and `wp_postmeta`, and variations are stored as separate entries.
* WooCommerce registers product-related post types like `product` and `product_variation`.

Why it matters:

* If your source platform treats variants, options, and attributes differently, mapping must preserve how customers select and purchase.
* Variation-heavy catalogs are not just a “data size” issue. They are a “behavior integrity” issue.

#### Catalog organization

WooCommerce uses WordPress taxonomies and relationships, including:

* Product categories (`product_cat`) and product tags (`product_tag`)
* Taxonomy tables (`wp_terms`, `wp_term_taxonomy`, `wp_term_relationships`) support category and attribute structure.

Why it matters:

* Category structure and product assignment can migrate, but navigation depends on how your theme and menus present it.
* Category naming and hierarchy decisions become “storefront UX” decisions during migration.

#### Custom data and plugin-driven fields

WooCommerce stores many details in `wp_postmeta` (including prices, SKU, and attributes), and plugins can add their own data structures. [WooCommerce+1](https://woocommerce.com/document/search-your-woocommerce-site-database/?utm_source=chatgpt.com)

Why it matters:

* “Custom fields” can be easy to store but hard to use consistently across themes, filters, feeds, and search.
* Plugin-driven fields may not map cleanly unless you define what must remain true after migration.

#### Orders and order history storage

Historically, WooCommerce stored orders using WordPress posts and postmeta.

WooCommerce introduced High-Performance Order Storage (HPOS), which uses dedicated order tables, and it is enabled by default for new installations from WooCommerce 8.2 onward.

Why it matters:

* Order history can be stored differently depending on whether HPOS is used.
* Extension compatibility can affect how orders and related records behave when HPOS is enabled.

#### SEO inputs: permalinks and URL structure

WooCommerce URL structure is controlled through WordPress permalinks, with specific bases for product categories, tags, and products.

Why it matters:

* URL patterns can differ widely between stores.
* URL continuity planning becomes important when you change permalink structures during a migration.

#### Conclusion

WooCommerce data is highly flexible because it inherits WordPress structures and plugin extensibility. That same flexibility is why mapping and validation matter.

If your store has important custom fields or plugin-managed product logic, request **Next-Cart to run a Demo Migration** with your sample data to confirm what migrates cleanly versus what needs Custom Jobs.
