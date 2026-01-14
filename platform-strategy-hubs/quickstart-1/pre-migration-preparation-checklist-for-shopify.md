# Pre-migration Preparation Checklist for Shopify

Preparation for Shopify is mostly about structure and dependencies: variants, collections, custom data, and app-driven behaviors.

This checklist is conceptual on purpose.

#### 1) Catalog audit

Focus on the products that drive revenue and risk:

* Best sellers and top traffic products
* Products with complex variants
* Products where options are inconsistent or messy
* Products with variant-specific images

**Goal**: identify what must remain true in Shopify for buying behavior.

#### 2) Collection and navigation plan

Shopify uses collections as a primary organizing layer.

**Plan**:

* Which collections matter most for discovery
* Whether collections are curated (manual) or rule-based (smart)
* Which browse paths must remain intuitive after launch

#### 3) Custom data inventory

List custom fields and where they are used:

* Product page display
* Filtering and discovery
* Feeds, integrations, or reporting

Shopify supports custom data via metafields and structured definitions.

**Goal**: decide what must become Shopify metafields and what can be retired or rebuilt.

#### 4) App and integration inventory

Apps often hold business logic and data:

* reviews, loyalty, subscriptions, B2B rules, bundles, personalization, feeds

**Goal**: define which app-driven data must be preserved and which will be replaced.

#### 5) URL continuity and redirect planning

If URLs will change, define:

* Priority pages (categories, best sellers, top landing pages)
* Redirect coverage and limitations within Shopify’s redirect rules

#### 6) Timing and validation plan

Avoid last-minute QA by defining:

* A demo validation sample
* Who signs off on variant correctness, navigation, and SEO continuity
* A launch monitoring owner for early stabilization

#### Conclusion

Preparation for Shopify is preparation for structure. The earlier you define variant behavior, collections, custom data, and URL continuity, the smoother the project becomes.

If your team is unsure what to prioritize, validate a focused demo sample (complex variants, top collections, priority URLs) before you lock a go-live window.
