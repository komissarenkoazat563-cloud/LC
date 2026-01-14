# BigCommerce Validation Priorities: What to Verify Most Carefully

Validation is how you confirm “data moved” becomes “store behaves correctly.” For BigCommerce, the highest-value validation focuses on catalog behavior and browsing structure.

#### Priority 1: Variant integrity

**Validate**:

* Variants represent the correct sellable SKUs
* Pricing and inventory behave at the correct level (variant vs base)
* Option combinations match purchase behavior

#### Priority 2: Modifier behavior for customizations

**Validate**:

* Customizations behave as modifiers when they are meant to be add-ons and do not represent inventory SKUs
* Modifiers do not accidentally replace variants or break selection flow

BigCommerce defines modifiers as customizations that do not change which variant is fulfilled and cannot be inventory-tracked as combinations.

#### Priority 3: Category browsing per storefront channel

**Validate**:

* Category assignments match browse expectations
* Category trees match channel-specific structure where applicable.

#### Priority 4: Custom fields, metafields, and filtering

**Validate**:

* Critical product custom fields are present and used where required.
* Filtering behavior works for the attributes you rely on, since filtering is tied to platform capabilities and configuration.

#### Priority 5: URL continuity and redirects

**Validate**:

* Priority URLs resolve correctly post-launch
* Redirect expectations are met using BigCommerce redirect capabilities.

#### Conclusion

BigCommerce validation should prioritize configurable products and browsing structure first. Those are the highest risk areas and the most visible to customers.

For maximum confidence with minimal effort, validate a **Demo Migration** sample by requesting Next-Cart perform it for you, including your most configurable products, top categories, and priority URLs.
