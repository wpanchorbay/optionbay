# Frontend Display

OptionBay is designed to provide a seamless and interactive experience for your customers directly on the product page. This section explains how the options are rendered and how they interact with the WooCommerce interface.

## Option Placement

By default, OptionBay hooks into the `woocommerce_before_add_to_cart_button` hook. This ensures that your custom options appear right before the "Add to Cart" button, which is the most natural position for product customizations.

- **Responsive Design:** All field types are fully responsive and will adapt to the width of your theme's product container.
- **Orientation:** You can choose between **Vertical** (stacked) and **Horizontal** (side-by-side) layouts in the [Global Settings](./settings).

## Interactive Features

### Live Price Updates
One of the core features of OptionBay is the live total display. As customers select options or type into fields:
- The price deltas are calculated instantly.
- A "Total" or "Option Total" display appears near the Add to Cart button.
- The main product price may also update depending on your theme's compatibility.

### Instant Conditional Logic
Fields with [Conditional Logic](./conditional-logic) will show or hide instantly based on user input. This keeps the form clean by only showing relevant fields.

### Real-time Validation
- **Required Fields:** If a required field is empty, the "Add to Cart" button will be disabled, and a notice will appear if the user tries to click it.
- **File Types:** File upload fields validate the file extension and size before the upload even begins.

## Field Styling

OptionBay uses clean, semantic HTML that inherits as much styling as possible from your active WordPress theme. This ensures a consistent look and feel across your store.

- **Labels:** Inherit your theme's heading or label styles.
- **Inputs:** Dropdowns, text fields, and checkboxes will match your theme's default input styling.
- **Swatches:** Color and Image swatches have their own dedicated styling, which can be customized via the [Global Settings](./settings).

## Customization

If you need to further customize the look of your options, you can use the **Custom Class** setting on individual fields to target them with your own CSS in your theme's stylesheet.
