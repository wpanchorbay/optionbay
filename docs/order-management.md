# Order Management

For store administrators, OptionBay makes it easy to view and process custom product selections directly within the WordPress dashboard. All customer choices are permanently stored and accessible for fulfillment.

## Viewing Customer Selections

To view the options selected for an order:
1. Navigate to **WooCommerce > Orders**.
2. Click on the order you wish to view.
3. In the **Item List**, you will see the selected options listed under each product line item.

### How It Looks
Each addon selection appears as a key-value pair below the product name:

| Key | Value |
| :--- | :--- |
| Engraving Text | Hello World |
| Size | Large (+$5.00) |
| Gift Wrapping | Yes (+$10.00) |
| Color | Midnight Blue |
| Logo | [my-logo.png](#) (clickable link) |

### Data Storage
OptionBay saves selections as **Order Item Meta**. This means:
- The data is permanently attached to the specific order item.
- It will remain available even if you delete the original Option Group or the Product.
- Each selection is stored as a separate meta entry with the field's **Label** as the meta key and the customer's **selection** as the meta value.

## Handling File Uploads

If your customer uploaded a file (e.g., a logo for a custom print):
- The file name will be shown in the order details.
- The name will be a **clickable link** that opens the file in a new browser tab.
- Files are stored in your WordPress **Media Library** under the standard upload directory, making them easy to manage, download, and access for fulfillment.

> [!TIP]
> You can access uploaded files directly from the WordPress Media Library if you need to download them in bulk for fulfillment. Search for the filename shown in the order.

## Fulfillment Workflow

The custom selection data is available to other plugins and integrations that read WooCommerce order item meta:

| Integration | Compatibility |
| :--- | :--- |
| **PDF Invoice Plugins** | Most WooCommerce PDF Invoicing plugins (like WooCommerce PDF Invoices & Packing Slips) will automatically include the OptionBay meta data on the generated invoice. |
| **Shipping Platforms** | Platforms like ShipStation that pull order item data will generally see these selections as line item properties. |
| **REST API** | The selections are accessible through the WooCommerce REST API as standard order item meta, making custom integrations straightforward. |

## Price Integrity

> [!IMPORTANT]
> The prices saved in the order are **"frozen"** at the time of purchase. If you change the price of an addon later, it will **not** affect orders that have already been placed. This ensures accurate historical records and prevents retroactive price changes from affecting completed transactions.

## Manual Order Creation

When creating an order manually from the backend:
1. Add the product to the order.
2. You can manually add meta keys and values to the line item to match the customer's needs if they communicated their choices outside of the website (e.g., via email or phone).
3. Note: The interactive Addon Builder interface is not currently available for manual backend orders — it is designed for customer-facing frontend use only.

## Next Steps
- [Cart & Checkout Integration](./cart-checkout)
- [Global Settings](./settings)
