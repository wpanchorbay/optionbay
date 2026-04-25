# Textarea Field

The **Textarea** field provides a larger, multi-line text box for customers to enter longer messages or detailed instructions. Unlike the single-line Text Input, the Textarea expands vertically to accommodate paragraphs of text.

## Common Use Cases
- Long gift notes or personal messages
- Special delivery or handling instructions
- Detailed customization requirements (e.g., cake decoration descriptions)
- Custom product specifications or notes to the seller

## Field Settings

When you add a Textarea field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the textarea on the product page (e.g., "Gift Message"). |
| **Description** | Optional help text shown below the field to guide the customer (e.g., "Maximum 200 characters"). |
| **Required** | When checked, the customer must enter text before adding the product to the cart. |

### Placeholder
You can set **Placeholder** text that appears as faded hint text inside the textarea (e.g., "Type your full message here..."). This text disappears as soon as the customer starts typing.

### Pricing
Since the Textarea is not an options-based field, pricing is configured at the **field level**:

| Setting | Description |
| :--- | :--- |
| **Price Type** | Choose how the field affects the product price. Available types: **No Price**, **Flat Fee**, **Percentage of Base**, **Per Character**, or **Formula**. |
| **Price Amount** | The numeric value to apply. |
| **Formula** | (Only when Price Type is "Formula") A math expression using placeholders like `[value]`, `[char_count]`, `[base_price]`, and `[quantity]`. |

### Restrictions
| Setting | Description |
| :--- | :--- |
| **Min Length** | The minimum number of characters the customer must enter. |
| **Max Length** | The maximum number of characters allowed. Useful for limiting the length of engraving or embroidery text. |

> [!TIP]
> Combine **Per Character** pricing with a **Max Length** restriction to let customers know exactly what their customization will cost. For example, "Each character costs $0.25, maximum 150 characters."

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, you might only show a "Special Instructions" textarea when the customer selects "Custom Order" from a dropdown.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
