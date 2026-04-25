# Image Swatch Field

The **Image Swatch** field presents options as clickable thumbnail images instead of text labels. This is highly effective for visual products where a picture communicates the option far better than words.

## Common Use Cases
- Selecting a fabric pattern or textile print
- Choosing a specific design, logo, or illustration to be printed
- Selecting a product style or shape visually
- Choosing a material texture (e.g., leather grain, wood finish)

## Field Settings

When you add an Image Swatch field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the swatch grid (e.g., "Choose Your Pattern"). |
| **Description** | Optional help text shown below the swatches. |
| **Required** | When checked, the customer must select one swatch before adding the product to the cart. |

### Display Style
You can choose how the swatch options are rendered on the frontend:

| Style | Description |
| :--- | :--- |
| **Swatch Only** | Shows just the image thumbnail. Clean and minimal. |
| **Swatch + Label** | Shows the image thumbnail with the choice label text below it. Useful when images alone might be ambiguous. |

### Choices (Options)
You must define at least one choice. Each choice has the following columns:

| Column | Description |
| :--- | :--- |
| **Image** | Click the image placeholder to open the WordPress Media Library and select an image. The thumbnail version of the image is used for the swatch. |
| **Label** | The text identifying this choice (e.g., "Floral Print"). The **Value** is automatically generated from the label. |
| **Price** | The numeric amount to add to the product price when this swatch is selected. Only visible when Price Type is not "No Price". |
| **Price Type** | How this choice affects pricing. Options: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. Each choice can have its own independent price type. |
| **Weight** | Additional shipping weight to add when this choice is selected. |

> [!TIP]
> The **size and border-radius** of image swatches are configured globally in **WooCommerce > Settings > OptionBay**. Use the "Image Swatch Size" and "Image Swatch Radius" settings to match your theme's aesthetic.

You can add new choices using the **+ Add Choice** button and remove them using the trash icon.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Choose Your Pattern" image swatch only when the customer selects "Custom Fabric" from a material dropdown.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
