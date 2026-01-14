# Entity Points Explained: How Migration Scope Is Measured

Migration pricing often fails beginners for one reason: simple counts do not reflect real effort.

Two stores can have the same number of products, but very different workload and risk. A store with deep order history, heavy relationships, and more content usually requires more processing and validation than a store with similar product volume but limited history.

That is why Next-Cart uses **Entity Points**.

#### What are Entity Points

Entity Points are Next-Cart’s weighted way of measuring migration scope based on the four most important data types:

* **Products**
* **Orders**
* **Blog Posts**
* **Customers**

Instead of treating each entity type as equal, Entity Points apply weights to reflect effort and risk.

#### **The Entity Points formula**

Each core entity type has a coefficient (weight):

* Products: **1.0**
* Orders: **0.8**
* Blog Posts: **0.6**
* Customers: **0.5**

{% code overflow="wrap" fullWidth="true" %}
```
Entity Points = (Products × 1.0) + (Orders × 0.8) + (Blog Posts × 0.6) + (Customers × 0.5)
```
{% endcode %}

**Example calculation**

If your store has:

* 500 products
* 600 orders
* 100 blog posts
* 100 customers

Entity Points = (500 × 1.0) + (600 × 0.8) + (100 × 0.6) + (100 × 0.5)\
\= **1,090 Entity Points**

That total is what you use to choose the plan that fits the size of a migration run.

#### What counts, and what does not

A common misconception is that Entity Points represent everything that migrates. They do not.

Entity Points are a sizing method based on the “big four” core entities. Many supporting data structures can still be migrated as part of service scope but do not increase the Entity Points calculation, such as:

* Categories and subcategories
* Product images (main, gallery, in-description images)
* Reviews and ratings
* Manufacturers and brands
* Coupons and discount codes
* Taxes and tax rules
* Customer groups and segmentation fields (where supported)

A practical way to remember this: Entity Points help size the major workload drivers, not charge separately for every supporting element.

#### **Next-Cart's Entity Points Plan Pricing**

#### **Crucial Information You Need to Focus**

Your Migration Service and Entity Points Plan are specifically licensed for one distinct platform pairing (Source → Target).

This means the powerful migration solution you purchase from Next-Cart is tailored for the specific platforms you select.

_Let's look at an example:_

Imagine you choose the **Standard Migration Service** and the **Pro+ Entity Points Plan** to move your data from **Shopify** to **WooCommerce**.

* **The Licensed Migration Pair**: Shopify → WooCommerce
* **The Entity Points Plan**: Pro+, handles up to 1,024,000 Entity Points
* **The Migration Service**: Standard

_What does this mean for you?_

Your purchase authorizes data migration only in that **specific direction (Shopify** to WooCommerce). It cannot be used for **reverse migration** (WooCommerce to Shopify) or applied to a completely **different pair** (e.g., Shopify to Shift4Shop, Shopify to Magento, etc.).

To initiate a migration for a new platform pairing, you will need to acquire a separate Migration Service and Entity Points Plan dedicated to that specific new pair.

#### A critical detail: Entity Points apply per migration run

Entity Points are a limit per individual migration run, not a lifetime pool that gets consumed.

This matters if you run:

* A Full Migration, then
* One or more **Recent Data Migrations** to sync new orders, customers, or products before go-live

You can run Recent Data Migration multiple times during your schedule, as long as each run stays within your plan’s Entity Points.

#### How pricing scales for extremely large migrations

For very large migrations, additional upgrade logic can apply.

If a plan surpasses **1,024,000 Entity Points**, an additional **$50** is charged for each extra **100,000 Entity Points**.

#### Best practices for accurate sizing

* Use admin totals, not guesses
* Pull product, customer, order, and blog post counts from your current store
* Treat Entity Points as a planning tool, not only a pricing number
* Estimate Recent Data Migration separately, since it is typically much smaller than the full run

#### Conclusion

Entity Points are designed to make migration scope predictable by reflecting effort and risk, not just raw counts.

If you want the fastest way to confirm scope and reduce estimation errors, export your migration data or check the total entity through your store admin dashboard first, then use your real counts to choose a plan with confidence.

#### FAQs

<details>

<summary><strong>Do images, categories, or reviews increase Entity Points?</strong></summary>

No. Entity Points are calculated from products, orders, blog posts, and customers only. Supporting data may still be included in scope depending on platform support.

</details>

<details>

<summary><strong>Do I need a new plan for Recent Data Migration?</strong></summary>

**Do I need a new plan for Recent Data Migration?**

Not automatically. Because the plan is per run, you only need an upgrade if a single Recent Data Migration run exceeds your current plan’s Entity Points.

Plus, you'll only be charged the difference between your existing plan and the upgraded one, so there’s no need to pay full price again.

As a bonus, your 1-year license will be extended by an additional month, ensuring you get even more value.<br>

</details>

<details>

<summary><strong>Is Next-Cart pricing a subscription?</strong></summary>

Next-Cart is a one-off payment model for your migration project, not a recurring monthly subscription.

The migration service purchase will have a 1-year license with a 1-month extension when upgrading the Entity Point plan.

</details>
