# Number Input Field

The **Number Input** field restricts the customer's input strictly to numeric values. The browser renders a native number spinner, and OptionBay enforces minimum, maximum, and step constraints both on the frontend and during server-side validation.

## Common Use Cases
- Custom dimensions (length, width, height in cm or inches)
- Selecting a quantity of a specific add-on item
- Specifying an age, weight, or other measurement
- Entering a custom number for pricing calculations (e.g., square footage)

## Field Settings

When you add a Number field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the input on the product page (e.g., "Width (cm)"). |
| **Description** | Optional help text shown below the input (e.g., "Enter a value between 10 and 200"). |
| **Required** | When checked, the customer must enter a number before adding the product to the cart. |

### Placeholder
You can set **Placeholder** text that appears inside the number input (e.g., "Enter width").

### Pricing
Since the Number field is not an options-based field, pricing is configured at the **field level**:

| Setting | Description |
| :--- | :--- |
| **Price Type** | Choose how the field affects the product price. Available types: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. |
| **Price Amount** | The numeric value to apply. |
| **Formula** | (Only when Price Type is "Formula") A math expression using placeholders like `[value]`, `[base_price]`, and `[quantity]`. Example: `[value] * 2.50` charges $2.50 per unit of the entered number. |

> [!TIP]
> The **Formula** price type is especially powerful with number fields. For example, if your customer enters the square footage of a room, you can use `[value] * 3.00` to charge $3.00 per square foot.

### Restrictions
| Setting | Description |
| :--- | :--- |
| **Min** | The lowest numeric value the customer can enter. |
| **Max** | The highest numeric value the customer can enter. |
| **Step Value** | Defines the legal number intervals. A step of `0.5` allows `1.0`, `1.5`, `2.0`, etc. A step of `1` only allows whole numbers. Defaults to `1`. |

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Width" number field only when the customer selects "Custom Size" from a dropdown.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
