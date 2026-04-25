# Cart & Checkout Integration

OptionBay ensures that all customer customizations follow the shopper through their entire journey — from the initial "Add to Cart" to the final checkout confirmation and beyond.

## How It Works

When a customer selects options and clicks "Add to Cart", OptionBay processes the data through a 5-stage pipeline:

1. **Validation:** All required fields and constraints are checked server-side.
2. **Data Storage:** The selected options are attached to the cart item as session data.
3. **Price Calculation:** Addon prices are calculated and added to the product's base price.
4. **Display:** The selected options are shown in the cart and checkout summaries.
5. **Order Storage:** On checkout, the data is permanently saved as order item meta.

## The Cart Page

When a product with custom options is added to the cart, OptionBay attaches the selection data to the cart item.

### Displaying Options
In the standard WooCommerce cart template, the selected options appear directly below the product name as a list of key-value pairs:

| Format | Example |
| :--- | :--- |
| **Text/Textarea** | `Engraving: Hello World` |
| **Select/Radio** | `Size: Large` |
| **Checkbox** | `Extras: Gift Wrap, Insurance` |
| **Color Swatch** | `Color: Midnight Blue` |
| **Image Swatch** | `Pattern: Floral Print` |
| **Single Checkbox** | `Rush Processing: Yes` |
| **File Upload** | `Logo: my-logo.png` (clickable link) |
| **Number** | `Width (cm): 42` |
| **Email** | `Recipient: friend@example.com` |

### Price Adjustments
The product price shown in the cart reflects the **total price** including all selected addons:
- If a product is $100 and a $20 "Gift Wrap" addon is selected, the cart will display the item price as **$120.00**.
- Multiple addons are cumulative. A $100 product with a $20 wrap and a $5 card shows as **$125.00**.
- This ensures that the cart subtotal and grand total are always accurate.

### Weight Adjustments
If you have configured **Weight** values for your fields or options, the total weight of the cart item is automatically updated. This is critical for stores that use weight-based shipping methods (like UPS, FedEx, or Weight-Table rate shipping).

> [!IMPORTANT]
> Weight adjustments happen at the cart item level. Each addon's weight value is added to the product's base weight, and WooCommerce's shipping calculator uses the updated total weight.

## The Checkout Page

On the checkout page, the selected options continue to be displayed in the **"Your Order"** review section. This gives customers one final chance to verify their customizations before completing the purchase.

The pricing shown at checkout is identical to the cart — all addon costs are included in the line item price.

## Thank You Page & Customer Emails

After the order is placed:

1. **Thank You Page:** The customer sees their selected options in the order details table on the confirmation page.
2. **Order Confirmation Email (Customer):** The customer receives an email containing the full list of custom options for each line item, so they have a personal record of their choices.
3. **New Order Email (Admin):** The store administrator receives an email with all the custom option details, making it easy to begin fulfillment.

## Modifying Options

Currently, to change the selected options, a customer must:
1. Remove the item from their cart.
2. Return to the product page.
3. Re-select their options and add the product again.

This ensures that all conditional logic, pricing calculations, and validation rules are properly re-evaluated.

## Next Steps
- [Order Management for Admins](./order-management)
- [Frontend Display Details](./frontend-display)
