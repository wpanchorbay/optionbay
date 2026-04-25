# Frontend Display

OptionBay is designed to provide a seamless and interactive experience for your customers directly on the product page. This section explains how the options are rendered, how they interact with the WooCommerce interface, and how you can customize their appearance.

## Option Placement

By default, OptionBay hooks into the `woocommerce_before_add_to_cart_button` action. This ensures that your custom options appear right before the "Add to Cart" button, which is the most natural position for product customizations.

- **Responsive Design:** All field types are fully responsive and will adapt to the width of your theme's product container.
- **Orientation:** You can choose between **Vertical** (stacked) and **Horizontal** (side-by-side) layouts for radio and checkbox groups in the [Global Settings](./settings).

> [!NOTE]
> If your theme uses a custom product template that does not fire the standard `woocommerce_before_add_to_cart_button` hook, OptionBay fields may not appear automatically. Contact your theme developer or use a manual template override to add the hook.

## Interactive Features

### Live Price Updates
One of the core features of OptionBay is the live total display. As customers select options or type into fields:
- The price deltas are calculated instantly using JavaScript on the client side.
- An **Option Total** display appears near the Add to Cart button showing the real-time cost of all selected addons.
- The combined total (base price + addon prices) updates dynamically so customers always know the final cost before adding to cart.

### Instant Conditional Logic
Fields with [Conditional Logic](./conditional-logic) will show or hide instantly based on user input. There is no page reload — the transitions happen smoothly in real time. This keeps the form clean by only showing relevant fields, creating a personalized shopping journey.

### Real-time Validation
- **Required Fields:** If a required field is empty, the "Add to Cart" button will be disabled. A red asterisk (*) appears next to required field labels, and a notice will appear if the user tries to submit without completing them.
- **Number Constraints:** Number fields enforce min/max/step constraints via the native browser controls.
- **File Types:** File upload fields validate the file extension and size on the client side before the upload begins, and again on the server side for security.

## Field Styling

OptionBay uses clean, semantic HTML that inherits as much styling as possible from your active WordPress theme. This ensures a consistent look and feel across your store.

| Element | Behavior |
| :--- | :--- |
| **Labels** | Inherit your theme's label or paragraph styles. Font size is configurable in [Global Settings](./settings). |
| **Inputs** | Dropdowns, text fields, and number inputs match your theme's default input styling. Font size is configurable. |
| **Radio & Checkboxes** | Use native browser rendering, styled by your theme. |
| **Color Swatches** | Rendered as colored blocks with configurable size and border-radius via [Global Settings](./settings). |
| **Image Swatches** | Rendered as thumbnail images with configurable size and border-radius via [Global Settings](./settings). |
| **Descriptions** | Shown as small helper text below each field. |

## Customization

If you need to further customize the look of your options, you can add custom CSS to your theme's stylesheet targeting the OptionBay field containers. The HTML structure uses semantic class names prefixed with `optionbay-` for easy targeting.

## Next Steps
- [Learn about Cart & Checkout Integration](./cart-checkout)
- [Configure Global Settings](./settings)
