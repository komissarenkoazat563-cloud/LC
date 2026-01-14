# PrestaShop Validation Priorities: What to Verify Most Carefully

PrestaShop validation should be behavior-first. Modules and multistore context can change what customers experience, even if records exist in the database.

#### Priority 1: Combination integrity and purchase behavior

**Validate**:

* Customers can select the right combinations
* Pricing and stock behavior is correct across variations
* Key variation-dependent images and descriptions behave as expected

PrestaShop combinations represent attribute-driven variations.

#### Priority 2: Module-sensitive customer journeys

**Validate**:

* Promotions and pricing behavior in core buying paths
* Checkout behavior if modules influence it
* Any product customization flows

#### Priority 3: Multistore context outcomes

If multistore exists:

* Validate each store context separately
* Validate domain-specific or store-specific differences that matter to customers

#### Priority 4: SEO continuity and URL outcomes

**Validate**:

* Friendly URL behavior and canonical URL behavior align with expectations
* Priority URLs redirect correctly after launch based on your redirect plan and tooling

**Next-Cart insight**: This is where a Demo Migration is especially useful because it can reveal URL path changes early and help you plan redirect continuity confidently.

If SEO continuity is a primary concern, validate a **Demo Migration** sample that includes top traffic URLs and best sellers so redirect readiness is confirmed before go-live.
