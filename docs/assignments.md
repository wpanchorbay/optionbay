# Product Assignments

**Assignments** allow you to control exactly where your Option Groups appear on your storefront. OptionBay uses a rule-based system that gives you the flexibility to target your entire catalog or just a single specific product.

## Accessing Assignments

Assignment rules are managed within each **Option Group**. When editing a group, look for the **Assignments** section (usually located in the sidebar or a secondary tab).

## Assignment Types

You can mix and match these rules to get the perfect coverage:

### 1. Global (All Products)
If enabled, this group will appear on every single product in your WooCommerce store. This is perfect for things like "Rush Processing" or "Gift Wrapping" that apply to everything you sell.

### 2. Specific Products
Search for and select individual products. The group will only appear on these specific items.

### 3. Product Categories
Select one or more categories. Any product assigned to these categories will automatically display this option group. This is the most efficient way to manage options for large collections (e.g., all "T-Shirts" get the "Sizing" group).

### 4. Product Tags
Similar to categories, you can target products based on their WordPress tags.

## Priority & Ordering

When a product has multiple option groups assigned to it, you can control the order in which they appear on the product page using the **Priority** setting.

- **How it works:** Groups are sorted numerically based on their priority value.
- **Rule of Thumb:** Lower numbers appear **first**. For example, a group with priority `1` will appear above a group with priority `10`.
- **Default Value:** If no priority is set, groups default to `10`.

## Assignment Exclusions

Exclusions allow you to create "negative" rules. This is incredibly powerful for handling exceptions to global or category-wide rules.

### How Exclusions Work
If a group is both **included** (e.g., via a "Global" rule) and **excluded** (e.g., via a "Specific Product" exclusion), the **exclusion always wins**. The group will not be displayed on that product.

### Common Use Cases
- **Category Exception:** You want a "Size Chart" group on all products in the "Apparel" category, *except* for "Socks". You would add an inclusion for the "Apparel" category and an exclusion for the "Socks" category.
- **Global Exception:** You have a "Gift Wrapping" option on all products, but you want to hide it for "Digital Downloads". You would enable the "Global" inclusion and add an exclusion for the "Digital" category.

## Troubleshooting Assignments

If a group isn't appearing on a product as expected, check the following:
1. **Status:** Ensure the Option Group is set to **Published**, not Draft.
2. **Exclusions:** Check if there is an active Exclusion rule targeting that specific product, category, or tag. Remember: **Exclusions always override inclusions.**
3. **Cache:** If you are using a caching plugin (like WP Rocket), you may need to clear your cache after changing assignment rules.
4. **Hierarchy:** Remember that assignments are additive. If a product is in the "T-Shirts" category and you have a group assigned to that category, it will appear unless an exclusion is present.

## Next Steps
- [Learn about Conditional Logic](./conditional-logic)
- [Managing Global Settings](./settings)
