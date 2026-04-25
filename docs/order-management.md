# Order Management

For store administrators, OptionBay makes it easy to view and process custom product selections directly within the WordPress dashboard.

## Viewing Customer Selections

To view the options selected for an order:
1. Navigate to **WooCommerce > Orders**.
2. Click on the order you wish to view.
3. In the **Item List**, you will see the selected options listed under each product.

### Data Storage
OptionBay saves selections as **Order Item Meta**. This means the data is permanently attached to the specific order item and will remain available even if you delete the original Option Group or the Product.

## Handling File Uploads

If your customer uploaded a file (e.g., a logo for a custom print):
- The file name will be shown in the order details.
- The name will be a **clickable link** that opens the file in a new tab.
- Files are stored in your WordPress Media Library, making them easy to manage and access for fulfillment.

## Fulfillment Workflow

The custom selection data is available to other plugins and integrations:
- **PDF Invoices:** Most WooCommerce PDF Invoicing plugins will automatically include the OptionBay meta data on the generated invoice.
- **Shipping Platforms:** Platforms like ShipStation that pull order item data will generally see these selections as line item properties.

## Manual Order Creation

When creating an order manually from the backend:
1. Add the product to the order.
2. You can manually add meta keys and values to match the customer's needs if they communicated them outside of the website.
3. Note: The interactive Addon Builder is not currently available for manual backend orders; it is designed for customer-facing frontend use.

## Technical Notes

- **Meta Keys:** The meta keys used in the database match the **Field Labels** you defined in the Addon Builder.
- **Price Integrity:** The prices saved in the order are "frozen" at the time of purchase. If you change the price of an addon later, it will not affect orders that have already been placed.
