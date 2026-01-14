# BigCommerce Data Model Differences: What Changes and Why It Matters

A successful BigCommerce migration is not only moving data. It is preserving meaning:

* What is a real inventory SKU (variant)
* What is a customer customization (modifier)
* How shoppers browse (categories and category trees)
* How custom data is used (custom fields and metafields)
* How URLs and redirects preserve continuity

#### Variants vs modifiers (a critical BigCommerce distinction)

BigCommerce’s V3 catalog model clearly separates:

* **Variant options** that generate sellable variants (inventory-oriented SKUs)
* **Modifiers** that represent customization choices and do not generate variants, and you cannot track inventory for combinations of modifier values.

Why it matters:

* If your source platform treats customizations as variants, you may need to restructure to avoid creating an unmanageable number of SKUs.
* If you need inventory tracking per combination, that pushes you toward variants, which have practical caps.

#### Variant scale and option value scale

BigCommerce supports complex catalogs at a practical scale:

* Up to **600 SKUs per product** is referenced as a “complex catalog” capability.
* BigCommerce caps the **total number of values per option at 250** (creating more returns an error).

Why it matters:

* Large configurators can exceed variant SKU limits quickly, so planning variants vs modifiers is a major risk control lever.
* Very large option value sets (for example long pick lists) need early validation.

#### Categories and category trees (how browsing structure works)

BigCommerce catalogs use categories that can be organized into **category trees**, and stores can have multiple trees tied to different storefront channels.

Why it matters:

* If your current store has different storefronts or channels, category tree planning becomes part of data migration planning.
* “Same category name” does not always mean “same browsing experience,” so validation should focus on top browse paths.

BigCommerce also caps the number of categories a product can belong to at **1,000**.

#### Custom data: custom fields and metafields

BigCommerce supports product custom fields and supports “metafields” as key-value style attributes across multiple objects.

Variants can have metafields as well, and BigCommerce provides endpoints for managing them.

Why it matters:

* If your current store depends on custom attributes for filtering, feeds, or display, you need to define what must exist in BigCommerce and where it must appear.

#### Content and SEO-relevant structures

BigCommerce storefront routing can represent products, categories, brands, pages, and blog content, and redirects can be represented as redirect nodes.

Why it matters:

* Content and URL continuity planning should be deliberate, especially if your source platform has deeply indexed URLs.

#### Conclusion

BigCommerce’s model is powerful, but it rewards upfront decisions about variants vs modifiers, category structure, and how custom data is used.

If your catalog risks exceeding variant SKU limits or depends heavily on custom attributes, use a **Demo Migration** (run it yourself or request Next-Cart perform it for you) to validate how products, variants, modifiers, and category assignments translate before you lock scope.
