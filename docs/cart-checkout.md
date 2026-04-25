# Cart & Checkout Integration

OptionBay ensures that all customer customizations follow the shopper through their entire journey—from the initial "Add to Cart" to the final checkout confirmation.

## The Cart Page

When a product with custom options is added to the cart, OptionBay attaches the selection data to the cart item.

### Displaying Options
In the standard WooCommerce cart template, the selected options will appear directly below the product name. 
- **Format:** `Label: Selection` (e.g., `Engraving: Hello World`).
- **File Uploads:** For file fields, a link to the uploaded file will be displayed.

### Price Adjustments
The product price shown in the cart will be the **Total Price**, including all selected addons. 
- If a product is $100 and a $20 "Gift Wrap" option is selected, the cart will display the item price as $120.
- This ensures that the cart subtotal and grand total are always accurate.

### Weight Adjustments
If you have configured **Weight Addition** for your fields, the total weight of the cart item will be updated. This is critical for stores that use weight-based shipping methods (like UPS, FedEx, or Weight-Table rates).

## The Checkout Page

On the checkout page, the selected options continue to be displayed in the "Your Order" review section. This gives customers one final chance to verify their customizations before completing the purchase.

## Thank You Page & Customer Emails

After the order is placed:
1. **Thank You Page:** The customer will see their selected options in the order details table on the confirmation page.
2. **Order Emails:** Both the Admin and the Customer will receive emails containing the full list of custom options for each line item.

## Modifying Options

Currently, to change the selected options, a customer must remove the item from their cart and add it again from the product page with the new selections. This ensures that all conditional logic and pricing calculations are re-validated correctly.
