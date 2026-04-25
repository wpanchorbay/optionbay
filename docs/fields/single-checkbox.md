# Single Checkbox Field

The **Single Checkbox** is a simple boolean toggle for straightforward Yes/No decisions. Unlike the multi-checkbox field which presents a list of choices, this field renders a single checkbox with a label.

## Common Use Cases
- "Add gift wrapping?" (+$5.00)
- "Include extended warranty?"
- "I agree to the terms and conditions"
- "Rush my order" (+$15.00)
- "Add insurance to my shipment?"

## Field Settings

When you add a Single Checkbox field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed next to the checkbox (e.g., "Add Gift Wrapping"). |
| **Description** | Optional help text shown below the checkbox (e.g., "We'll wrap your item in premium packaging"). |
| **Required** | When checked, the customer **must** tick this checkbox before adding the product to the cart. This is useful for mandatory agreements like terms and conditions. |

### Pricing
Since the Single Checkbox does not have a choices list, pricing is configured at the **field level**. The price is applied when the customer checks the box.

| Setting | Description |
| :--- | :--- |
| **Price Type** | Choose how the field affects the product price. Available types: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. |
| **Price Amount** | The numeric value to add when the box is checked. For example, enter `5` for a $5.00 gift wrapping fee. |
| **Formula** | (Only when Price Type is "Formula") A math expression using placeholders like `[value]`, `[base_price]`, and `[quantity]`. |

> [!TIP]
> Use a **Percentage of Base** price type to create add-ons that scale with the product price. For example, a 10% warranty on a $100 product adds $10.00, while the same warranty on a $500 product adds $50.00.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Rush Processing" checkbox only when the customer selects "Standard Shipping" from a shipping method dropdown.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
