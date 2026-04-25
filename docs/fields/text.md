# Text Input Field

The **Text Input** field allows customers to enter a single line of text. It's the most common field type and is ideal for collecting short, freeform information.

## Common Use Cases
- Monogram initials or custom engraving text
- Custom names or titles to be printed on a product
- Short gift messages or dedication text
- Custom order references or SKU codes

## Field Settings

When you add a Text Input field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the input on the product page (e.g., "Enter Your Name"). |
| **Description** | Optional help text shown below the input to guide the customer. |
| **Required** | When checked, the customer must fill in this field before adding the product to the cart. A red asterisk (*) will appear next to the label. |

### Placeholder
You can set **Placeholder** text that appears as faded hint text inside the input box (e.g., "Type your message here..."). This text disappears as soon as the customer starts typing.

### Pricing
Since the Text Input is not an options-based field, pricing is configured at the **field level**:

| Setting | Description |
| :--- | :--- |
| **Price Type** | Choose how the field affects the product price. Available types: **No Price**, **Flat Fee**, **Percentage of Base**, **Per Character**, or **Formula**. |
| **Price Amount** | The numeric value to apply. For a Flat Fee of $5.00, enter `5`. For a Percentage of 10%, enter `10`. |
| **Formula** | (Only when Price Type is "Formula") A math expression using placeholders like `[value]`, `[char_count]`, `[base_price]`, and `[quantity]`. Example: `[char_count] * 0.50` charges 50 cents per character. |

### Restrictions
| Setting | Description |
| :--- | :--- |
| **Min Length** | The minimum number of characters the customer must enter. |
| **Max Length** | The maximum number of characters allowed. |

> [!TIP]
> Use **Per Character** pricing together with **Min/Max Length** restrictions to create a controlled engraving or embroidery pricing model. For example, set a Min Length of 1, a Max Length of 20, and a Per Character price of $0.50.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, you could hide a "Custom Engraving Text" field until the customer selects "Yes" on a "Add Engraving?" checkbox.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
