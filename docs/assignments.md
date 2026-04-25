# Product Assignments

**Assignments** allow you to control exactly where your Option Groups appear on your storefront. OptionBay uses a rule-based system that gives you the flexibility to target your entire catalog, specific categories, individual tags, or hand-picked products.

## Accessing Assignments

Assignment rules are managed within each **Option Group**. When editing a group in the Addon Builder, look for the **Assignments** section located below the field builder area.

## Assignment Types

You can mix and match these rules to get the perfect coverage:

### 1. Global (All Products)
If enabled, this group will appear on **every single product** in your WooCommerce store. This is perfect for universal options that apply to everything you sell.

**Best for:** Rush Processing, Gift Wrapping, Insurance, Terms & Conditions.

### 2. Specific Products
Search for and select individual products by name. The group will only appear on these specific items.

**Best for:** Highly customized products that need unique options (e.g., a single "Custom Engraved Watch" product that needs an engraving text field).

### 3. Product Categories
Select one or more WooCommerce categories. Any product assigned to these categories will automatically display this option group.

**Best for:** Managing options at scale for entire collections. For example, all products in the "T-Shirts" category automatically get the "Sizing & Color" option group.

### 4. Product Tags
Similar to categories, you can target products based on their WordPress tags. This is useful when you need cross-category targeting.

**Best for:** Targeting products that share a trait across multiple categories (e.g., all products tagged "Personalizable" regardless of whether they're in "Mugs" or "T-Shirts").

## Priority & Ordering

When a product has multiple option groups assigned to it (e.g., both a "Gift Wrapping" global group and a "T-Shirt Sizing" category group), you can control the order in which they appear on the product page using the **Priority** setting.

| Setting | Description |
| :--- | :--- |
| **How it works** | Groups are sorted numerically by their priority value. |
| **Lower = First** | A group with priority `1` appears above a group with priority `10`. |
| **Default** | If no priority is set, groups default to `10`. |

> [!TIP]
> Use priorities like `5`, `10`, `15` instead of `1`, `2`, `3`. This leaves room to insert new groups between existing ones without having to renumber everything.

## Assignment Exclusions

Exclusions allow you to create **negative rules** — telling OptionBay where a group should **not** appear. This is incredibly powerful for handling exceptions to broad rules.

### How Exclusions Work
If a group is both **included** (e.g., via a "Global" rule) and **excluded** (e.g., via a "Specific Product" exclusion), the **exclusion always wins**. The group will not be displayed on that product.

### Common Use Cases

| Scenario | Inclusion | Exclusion |
| :--- | :--- | :--- |
| Gift wrap on everything except digital downloads | Global (All Products) | Category: "Digital Downloads" |
| Size chart on all apparel except socks | Category: "Apparel" | Category: "Socks" |
| Custom engraving on all jewelry except earrings | Category: "Jewelry" | Tag: "Earrings" |

## Troubleshooting Assignments

If a group isn't appearing on a product as expected, check the following:

1. **Status:** Ensure the Option Group is set to **Published**, not Draft. Draft groups are never shown on the frontend.
2. **Exclusions:** Check if there is an active Exclusion rule targeting that specific product, category, or tag. Remember: **Exclusions always override inclusions.**
3. **Cache:** If you are using a caching plugin (like WP Rocket, W3 Total Cache, or LiteSpeed Cache), you may need to clear your cache after changing assignment rules.
4. **Theme Hooks:** Your theme must fire the standard `woocommerce_before_add_to_cart_button` hook. Most themes do, but some custom page builders might require manual placement.

## Next Steps
- [Learn about Conditional Logic](./conditional-logic)
- [Managing Global Settings](./settings)
