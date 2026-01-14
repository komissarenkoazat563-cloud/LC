# When Custom Job Is Required: Common Real-World Scenarios

Many migration problems are not caused by “missing records.” They happen when data exists, but the meaning does not survive the move.

A **Custom Job** is required when standard mapping cannot preserve meaning, because your store uses non-standard data structures or business rules.

This article will help you identify when your project is likely to need Custom Jobs and what that means for service selection.

#### What a Custom Job is

A Custom Job is a defined piece of work that handles special requirements, such as:

* Migrating data that lives in third-party plugins, modules, or extensions
* Transforming data so it works in the target platform’s model
* Applying custom mapping rules beyond standard fields and relationships
* Selectively filtering or restructuring data so results match business needs
* Customize modifications to the data migration setting and infrastructure to suit the customer's request

Custom Jobs are most relevant when you need “behavior continuity”, not just “data presence.”

#### Common scenarios that require Custom Jobs

**Scenario 1: Third-party plugin or module data must be preserved**

Examples:

* Loyalty points systems
* Membership tiers
* Subscriptions metadata
* Reviews and user-generated content stored outside standard tables

If the data is owned by a third-party system, standard migration often cannot interpret it correctly without custom handling.

**Scenario 2: Custom-coded fields that drive storefront behavior**

Examples:

* Custom product fields used for filtering or special labels
* Custom pricing logic
* Special fulfillment flags that affect operations

If the field changes what customers see or what staff must do, it typically deserves Custom Job evaluation.

**Scenario 3: The target platform requires a different structure**

Sometimes the data is valid, but the model changes.\
Examples:

* What was a “variant” in one platform may need restructuring to remain purchasable in another
* What was stored as a free-form attribute may need to become structured custom data

When the structure changes, custom transformation can be the difference between “migrated” and “usable”.

**Scenario 4: Selective migration requirements**

Examples:

* Migrate only specific product sets or only certain customer cohorts
* Exclude discontinued catalog segments while preserving order history

Selective rules can be simple or complex. When they affect core relationships, they often require custom logic.

**Scenario 5: You need guaranteed outcomes for high-stakes data**

If certain entities must be correct for compliance, operations, or customer trust, custom handling is often justified even if standard migration could “mostly work.”

#### How to confirm whether you need Custom Jobs

The most reliable method is evidence-based planning:

1. Run a Demo Migration with complex data, not random samples
2. Identify gaps in meaning: missing relationships, wrong structure, unexpected behavior
3. Translate gaps into Custom Job requirements

A strong Custom Job request is specific:

* What data source owns the data
* Where it appears in the current store
* What it must become in the target store
* How you will validate success

#### Conclusion

Custom Jobs exist for a simple reason: complex stores cannot be migrated safely using only standard mappings.

If you suspect you need Custom Jobs, reach out via **Live Chat** to get expert support and consultation for your migration needs. You can also request **Next-Cart** perform a Demo Migration with your sample data and use the results to list your custom requirements clearly. That turns “we are complex” into a scoped plan you can execute.

#### FAQs

<details>

<summary><strong>Does needing a Custom Job mean the migration is risky?</strong></summary>

Not automatically. It means the project should be planned with the right service model and validation focus. The risk is ignoring custom requirements until late.

</details>

<details>

<summary><strong>Can I do a standard migration first and add Custom Jobs later?</strong></summary>

Sometimes, but many teams lose time by discovering custom gaps after they have already built the new store around incomplete assumptions. Demo-first planning usually reduces rework.

</details>

<details>

<summary><strong>What is the difference between Custom Jobs and configuration choices?</strong></summary>

Configuration choices adjust what the standard migration already supports. Custom Jobs handle work that the standard migration cannot do on its own.

</details>
