# Frequently Asked Questions

Find answers to common questions about OptionBay's features, compatibility, and setup.

## General Questions

### Is OptionBay compatible with my theme?
Yes! OptionBay is designed to be theme-agnostic. It uses standard WooCommerce hooks to display options and provides global settings for font sizes and orientation to help you match your theme's aesthetic. If you encounter layout issues, you can add custom CSS to your theme's stylesheet.

### Does OptionBay work with Variable Products?
Absolutely. OptionBay options will appear on both Simple and Variable product pages. You can even use assignment rules to show specific option groups only for certain variations (by targeting product tags or categories).

### Does this plugin slow down my site?
Performance was a primary goal during development. OptionBay uses a modern React-based admin that loads only when needed, and the frontend script is highly optimized to ensure it doesn't impact your Google PageSpeed scores.

## Pricing & Cart

### How are addon prices displayed in the cart?
Addon prices are added to the product's base price. On the cart and checkout pages, WooCommerce will show the updated total price. OptionBay also displays a clear list of the selected options and their individual costs (if configured) below the product name in the cart items.

### Can I use percentage-based pricing?
Yes. You can set a field's Price Type to **Percentage Increase**. This will calculate the addon cost based on the product's base price. For example, a 10% addon on a $100 product will add $10.00.

## Troubleshooting

### Why aren't my options appearing on the product page?
Please check the following:
1. **Option Group Status:** Is the group set to "Published"?
2. **Assignment Rules:** Have you correctly assigned the group to that product, category, or tag?
3. **WooCommerce Version:** Ensure you are running a supported version of WooCommerce.
4. **Theme Hooks:** Your theme must use the standard `woocommerce_before_add_to_cart_button` hook. Most themes do, but some custom builders might require manual placement.

### My "Add to Cart" button is disabled. Why?
This usually means a **Required Field** has not been filled out. Look for the red asterisk (*) next to field labels. Once all required options are selected, the button will automatically re-enable.

## Support

Need more help? Visit our website at [wpanchorbay.com](https://wpanchorbay.com) or reach out to our support team through the WordPress.org forums.
