# Email Input Field

The **Email Input** field provides a text input that is validated to ensure the customer enters a properly formatted email address. The browser enforces email format on the frontend, and OptionBay performs additional validation on the server side.

## Common Use Cases
- Collecting a recipient email for a digital gift card delivery
- Gathering a contact email for a personalized service (e.g., "Where should we send the proof?")
- Capturing an alternate email for order-related communications

## Field Settings

When you add an Email field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the input (e.g., "Recipient Email Address"). |
| **Description** | Optional help text shown below the input (e.g., "We'll send the e-gift card to this address"). |
| **Required** | When checked, the customer must enter a valid email before adding the product to the cart. |

### Pricing
Since the Email field is not an options-based field, pricing is configured at the **field level**:

| Setting | Description |
| :--- | :--- |
| **Price Type** | Choose how the field affects the product price. Available types: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. In most cases, email fields use "No Price" since they are informational. |
| **Price Amount** | The numeric value to add if a price type other than "No Price" is selected. |

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Recipient Email" field only when the customer selects "Send as Gift" from a radio button group.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
