# Dropdown Select Field

The **Select** field presents a classic dropdown menu where customers must choose exactly one option from a list. It's ideal when you have many choices but want to keep the interface clean and compact.

## Common Use Cases
- Selecting a size (Small, Medium, Large, X-Large)
- Choosing a material or finish (Wood, Metal, Plastic)
- Picking a delivery date or time slot
- Selecting a configuration or variant

## Field Settings

When you add a Select field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the dropdown (e.g., "Choose Your Size"). |
| **Description** | Optional help text shown below the dropdown. |
| **Required** | When checked, the customer must select an option before adding the product to the cart. |

### Choices (Options)
The core of the Select field is its **Choices** table. You must define at least one choice. Each choice has the following columns:

| Column | Description |
| :--- | :--- |
| **Label** | The text the customer sees in the dropdown menu (e.g., "Large"). The **Value** is automatically generated from the label as a lowercase, underscore-separated string (e.g., `large`). |
| **Price** | The numeric amount to add to the product price when this specific choice is selected. Only visible when Price Type is not "No Price". |
| **Price Type** | How this choice affects pricing. Options: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. Each choice can have its own independent price type. |
| **Weight** | Additional shipping weight to add when this choice is selected (affects shipping calculations). |

> [!NOTE]
> The **Per Character** price type is not available for individual choices since select options are predefined values, not freeform text.

You can add new choices using the **+ Add Choice** button and remove them using the trash icon on each row.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Sleeve Length" dropdown only when the customer selects "Long Sleeve" from another radio button field.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
