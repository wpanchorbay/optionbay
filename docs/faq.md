# Frequently Asked Questions

Find answers to common questions about OptionBay's features, compatibility, and setup.

## General Questions

### Is OptionBay compatible with my theme?
Yes! OptionBay is designed to be theme-agnostic. It uses the standard WooCommerce `woocommerce_before_add_to_cart_button` hook to display options and provides global settings for font sizes, swatch dimensions, and orientation to help you match your theme's aesthetic. If you encounter layout issues, you can add custom CSS to your theme's stylesheet targeting the `optionbay-` prefixed class names.

### Does OptionBay work with Variable Products?
Absolutely. OptionBay options will appear on both **Simple** and **Variable** product pages. You can even use assignment rules to show specific option groups only for certain product types by targeting product tags or categories.

### Does this plugin slow down my site?
Performance was a primary goal during development. OptionBay uses a modern React-based admin that loads only when needed (code splitting separates the builder from the settings page), and the frontend script is a lightweight vanilla JavaScript file that is highly optimized to ensure it doesn't impact your Google PageSpeed scores.

### How many Option Groups can I create?
There is no limit. You can create as many Option Groups as your store requires. Each group is stored as a WordPress custom post type, so performance scales naturally with your WordPress hosting.

### Can I duplicate an Option Group?
Yes. On the **Products > Options** page, hover over any group and click the **Duplicate** action. This creates an exact copy of the group — including all fields, pricing, conditional logic, and assignment rules — which you can then modify as needed.

## Pricing & Cart

### How are addon prices displayed in the cart?
Addon prices are added to the product's base price. On the cart and checkout pages, WooCommerce will show the updated total price. OptionBay also displays a clear list of the selected options and their individual costs below the product name in the cart items.

### What price types are available?
OptionBay supports the following price types:

| Price Type | Description |
| :--- | :--- |
| **No Price** | The field/option does not affect the product price. |
| **Flat Fee** | A fixed amount is added (e.g., +$5.00). |
| **Percentage of Base** | Calculates the addon cost based on the product's base price (e.g., 10% of a $100 product adds $10.00). |
| **Per Character** | Cost multiplied by the number of characters typed. Available only for Text and Textarea fields. |
| **Formula** | Advanced math-based pricing using placeholders like `[value]`, `[char_count]`, `[base_price]`, and `[quantity]`. |

### Are addon prices included in the order total?
Yes. All addon prices are fully integrated into the WooCommerce cart and checkout totals. They appear on the Thank You page, in customer and admin order emails, and in all PDF invoice plugins that read standard WooCommerce order item meta.

## Troubleshooting

### Why aren't my options appearing on the product page?
Please check the following:
1. **Option Group Status:** Is the group set to "Published"? Draft groups are never displayed.
2. **Assignment Rules:** Have you correctly assigned the group to that product, category, or tag? Check for any active exclusion rules that might be overriding an inclusion.
3. **WooCommerce Version:** Ensure you are running a supported version of WooCommerce (6.1+).
4. **Theme Hooks:** Your theme must use the standard `woocommerce_before_add_to_cart_button` hook. Most themes do, but some custom builders might require manual placement.
5. **Cache:** Clear any caching plugin caches after making changes to assignment rules.

### My "Add to Cart" button is disabled. Why?
This usually means a **Required Field** has not been filled out. Look for the red asterisk (*) next to field labels. Once all required options are selected or filled in, the button will automatically re-enable.

### My conditional logic isn't working. What should I check?
1. **Same Group:** Conditional logic only works between fields **in the same Option Group**. Cross-group rules are not supported.
2. **Value Match:** The value in the rule must exactly match what the field submits. For select/radio/checkbox fields, this is the option's **Value** (the auto-generated lowercase string), not the Label.
3. **Debug Mode:** Enable [Debug Mode](./settings) in the settings to see detailed logs that can help identify logic evaluation issues.

## Support

Need more help? Visit our website at [wpanchorbay.com](https://wpanchorbay.com) or reach out to our support team through the WordPress.org forums.
