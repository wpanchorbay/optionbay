# Radio Buttons Field

The **Radio** field allows customers to select exactly one option from a list, with all choices visible at once on the product page. Unlike a dropdown, customers can see every available option without clicking.

## Common Use Cases
- Selecting a primary color when only a few options exist
- Choosing between standard or expedited processing
- Picking a warranty tier (None, 1-Year, 3-Year)
- Selecting a product variant visually

## Field Settings

When you add a Radio field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the radio group (e.g., "Choose Processing Speed"). |
| **Description** | Optional help text shown below the field. |
| **Required** | When checked, the customer must select one of the radio options before adding the product to the cart. |

### Choices (Options)
You must define at least one choice. Each choice has the following columns:

| Column | Description |
| :--- | :--- |
| **Label** | The text displayed next to the radio button (e.g., "Express Shipping"). The **Value** is automatically generated from the label. |
| **Price** | The numeric amount to add to the product price when this choice is selected. Only visible when Price Type is not "No Price". |
| **Price Type** | How this choice affects pricing. Options: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. Each choice can have its own independent price type. |
| **Weight** | Additional shipping weight to add when this choice is selected. |

> [!TIP]
> The layout of radio buttons (vertical stack vs. horizontal row) is controlled by the **Options Orientation** setting in WooCommerce > Settings > OptionBay.

You can add new choices using the **+ Add Choice** button and remove them using the trash icon.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Warranty Level" radio group only when the customer checks an "Add Extended Warranty?" checkbox.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
