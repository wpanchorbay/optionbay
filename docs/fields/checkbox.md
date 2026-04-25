# Checkboxes Field

The **Checkbox** field allows customers to select one or **multiple** options from a predefined list. Each checked option's price is individually added to the product total, making this field ideal for add-on bundles.

## Common Use Cases
- Selecting extra toppings (e.g., Cheese, Pepperoni, Mushrooms)
- Choosing multiple add-on accessories (e.g., Cable, Case, Screen Protector)
- Opting into multiple services (e.g., Gift Wrapping + Express Processing + Insurance)
- Multi-select feature upgrades

## Field Settings

When you add a Checkbox field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the checkbox group (e.g., "Select Your Toppings"). |
| **Description** | Optional help text shown below the field (e.g., "Choose as many as you like"). |
| **Required** | When checked, the customer must select **at least one** checkbox option before adding the product to the cart. |

### Choices (Options)
You must define at least one choice. Each choice has the following columns:

| Column | Description |
| :--- | :--- |
| **Label** | The text displayed next to the checkbox (e.g., "Extra Cheese"). The **Value** is automatically generated from the label. |
| **Price** | The numeric amount to add to the product price when this specific checkbox is ticked. Only visible when Price Type is not "No Price". |
| **Price Type** | How this choice affects pricing. Options: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. Each choice can have its own independent price type. |
| **Weight** | Additional shipping weight to add when this choice is selected. |

> [!IMPORTANT]
> Because multiple checkboxes can be selected simultaneously, the **total addon price** is the sum of all individually checked options. For example, if "Extra Cheese" is $2.00 and "Pepperoni" is $3.00, and both are checked, the total addon cost is $5.00.

You can add new choices using the **+ Add Choice** button and remove them using the trash icon.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Choose Your Toppings" checkbox group only when the customer selects "Pizza" from a product type dropdown.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
