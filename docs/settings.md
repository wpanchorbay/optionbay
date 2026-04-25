# WooCommerce Settings

OptionBay integrates seamlessly into the WooCommerce ecosystem. All global configurations are managed directly within the WooCommerce settings interface, ensuring a native experience for store administrators.

## Accessing Settings

To manage your global configurations:
1. Go to **WooCommerce > Settings**.
2. Click on the **OptionBay** tab.

## General Settings

These settings control the visual appearance of your product options across the entire store.

### Options Orientation
Choose between **Vertical** and **Horizontal** layouts.
- **Vertical:** Options are stacked one on top of another (best for long lists).
- **Horizontal:** Options are displayed side-by-side (best for small sets of radio buttons or swatches).

### Font Sizes
Fine-tune the typography of your addons to match your store's theme:
- **Label Font Size:** The size of the field titles (e.g., "Choose Your Color").
- **Input Font Size:** The size of the text inside dropdowns, text fields, and checkbox labels.

### Swatch Customization
If you use Image or Color swatches, you can configure their dimensions globally:
- **Swatch Size:** The width and height of standard color swatches.
- **Swatch Radius:** The border-radius (e.g., `4px` for rounded corners or `50%` for circles).
- **Image Swatch Size:** The dimensions for image-based swatches.
- **Image Swatch Radius:** The border-radius specific to image swatches.

## System & Maintenance

Technical configurations for data management and troubleshooting.

### Preload Initial Data
This setting tracks whether the initial demo data (example option groups) has been loaded into your store. 
- If you want to re-run the demo data import (e.g., after deleting the example groups), uncheck this box and save. 
- The next time you activate the plugin or visit the Options page, the preloader will run again.

### Debug Mode
When enabled, detailed logs will be written to the database. This is helpful for troubleshooting conditional logic or pricing issues. 

> [!WARNING]
> Only enable Debug Mode when actively investigating an issue, as logging can impact site performance on very high-traffic stores.

### Data Purging
**Delete Data on Uninstall:** If checked, all OptionBay data (groups, assignments, and settings) will be permanently deleted from your database if the plugin is uninstalled. This is useful for keeping your database clean if you decide to stop using the plugin.

## Saving Changes

Unlike many React-based plugins, OptionBay uses the native **WooCommerce Save button**. 
- The button is located at the very bottom of the settings page.
- It will only become active once you have actually modified a setting.
- Clicking it will save your changes asynchronously without a full page refresh.
