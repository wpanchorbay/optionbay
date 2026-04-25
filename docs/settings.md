# WooCommerce Settings

OptionBay integrates seamlessly into the WooCommerce ecosystem. All global configurations are managed directly within the WooCommerce settings interface, ensuring a native experience for store administrators.

## Accessing Settings

To manage your global configurations:
1. Go to **WooCommerce > Settings**.
2. Click on the **OptionBay** tab.

## General Settings

These settings control the visual appearance of your product options across the entire store.

### Options Orientation
Choose between **Vertical** and **Horizontal** layouts for radio buttons and checkbox groups:

| Option | Description |
| :--- | :--- |
| **Vertical** | Options are stacked one on top of another. Best for long lists or when options have detailed labels. |
| **Horizontal** | Options are displayed side-by-side in a row. Best for small sets of 2-4 radio buttons or swatches. |

### Font Sizes
Fine-tune the typography of your addons to match your store's theme:

| Setting | Description |
| :--- | :--- |
| **Label Font Size** | The size of the field titles displayed above each input (e.g., "Choose Your Color"). Enter a CSS value like `14` (pixels). |
| **Input Font Size** | The size of the text inside dropdowns, text fields, and checkbox labels. Enter a CSS value like `13` (pixels). |

### Swatch Customization
If you use **Image Swatches** or **Color Swatches**, you can configure their dimensions globally:

| Setting | Description | Example |
| :--- | :--- | :--- |
| **Swatch Size** | The width and height of standard color swatches in pixels. | `36` |
| **Swatch Radius** | The border-radius of color swatches. Use `4px` for slightly rounded corners or `50%` for perfect circles. | `50%` |
| **Image Swatch Size** | The width and height of image-based swatches in pixels. | `48` |
| **Image Swatch Radius** | The border-radius specific to image swatches. | `4px` |

> [!TIP]
> To create perfectly circular color swatches, set the **Swatch Radius** to `50%`. For square swatches with slightly rounded edges, use a small pixel value like `4px`.

## System & Maintenance

Technical configurations for data management and troubleshooting.

### Debug Mode
When enabled, detailed logs will be written to the database. This is helpful for troubleshooting conditional logic evaluation, pricing calculations, or assignment rule resolution.

> [!WARNING]
> Only enable Debug Mode when actively investigating an issue. Logging can impact site performance on very high-traffic stores. Disable it once you've resolved the problem.

### Data Purging
**Delete Data on Uninstall:** If checked, all OptionBay data (groups, assignments, settings, and database tables) will be permanently deleted from your database when the plugin is **uninstalled** (not just deactivated).

> [!CAUTION]
> This action is irreversible. Only enable this if you are certain you want a clean removal. Deactivating the plugin does **not** delete data regardless of this setting — only full uninstallation triggers the purge.

## Saving Changes

Unlike many React-based plugins, OptionBay uses the native **WooCommerce Save button**:
- The button is located at the very bottom of the settings page.
- It will only become active once you have actually modified a setting.
- Clicking it will save your changes asynchronously without a full page refresh.
- A success toast notification will appear confirming your changes were saved.
