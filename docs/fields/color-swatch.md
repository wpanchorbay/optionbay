# Color Swatch Field

The **Color Swatch** field displays options as solid colored blocks that customers can click to select. This provides a visually intuitive way to choose colors without relying on text labels.

## Common Use Cases
- Selecting the primary color of a garment (Red, Blue, Green)
- Choosing a paint color for a custom product
- Picking a hardware finish (Gold, Silver, Matte Black, Rose Gold)
- Selecting a thread or ink color for embroidery or printing

## Field Settings

When you add a Color Swatch field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the swatch grid (e.g., "Select Your Color"). |
| **Description** | Optional help text shown below the swatches. |
| **Required** | When checked, the customer must select a color before adding the product to the cart. |

### Display Style
You can choose how the swatch options are rendered on the frontend:

| Style | Description |
| :--- | :--- |
| **Swatch Only** | Shows just the colored block. Clean and minimal. |
| **Swatch + Label** | Shows the colored block with the choice label text below it (e.g., "Ocean Blue"). Useful when exact color names matter. |

### Choices (Options)
You must define at least one choice. Each choice has the following columns:

| Column | Description |
| :--- | :--- |
| **Color** | Click the color preview block to open a native color picker. Select the exact hex color (e.g., `#FF5733` for a warm red-orange). |
| **Label** | The text identifying this choice (e.g., "Midnight Blue"). The **Value** is automatically generated from the label. |
| **Price** | The numeric amount to add to the product price when this color is selected. Only visible when Price Type is not "No Price". |
| **Price Type** | How this choice affects pricing. Options: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. Each choice can have its own independent price type. |
| **Weight** | Additional shipping weight to add when this choice is selected. |

> [!TIP]
> The **size and shape** of color swatches are configured globally in **WooCommerce > Settings > OptionBay**. Use the "Swatch Size" setting to control dimensions and "Swatch Radius" to switch between square (`4px`) and circular (`50%`) shapes.

You can add new choices using the **+ Add Choice** button and remove them using the trash icon.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Thread Color" swatch only when the customer checks an "Add Custom Embroidery?" checkbox.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
