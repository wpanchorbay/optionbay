# Conditional Logic

**Conditional Logic** allows you to dynamically show or hide fields based on the value of other fields in the same group. This creates a personalized, step-by-step experience for your customers — they only see the options that are relevant to their current selections.

## How It Works

Each field in an Option Group has a **Conditional Logic** section at the bottom of its settings panel. When you enable it, you define one or more **rules** that determine whether the field is visible or hidden.

### Key Concepts

| Concept | Description |
| :--- | :--- |
| **Action** | Choose whether to **Show** or **Hide** this field when the rules are met. |
| **Match Mode** | Choose **ALL** (every rule must be true) or **ANY** (at least one rule must be true). |
| **Rules** | One or more conditions that reference other fields in the same group. |

## Rule Components
A rule consists of three parts:
- **Target Field:** The other field you want to "watch" for changes.
- **Operator:** The comparison type. Supported operators include:
    - **equals:** Matches the value exactly.
    - **not equals:** Matches anything except the value.
    - **greater than:** (For numbers) Checks if the input is larger.
    - **less than:** (For numbers) Checks if the input is smaller.
    - **greater than or equals:** (For numbers) Checks if the input is larger or equal.
    - **less than or equals:** (For numbers) Checks if the input is smaller or equal.
    - **contains:** Checks if the value exists within the input (useful for text or multi-select).
    - **not contains:** Checks if the value is missing from the input.
    - **is empty:** Triggers if the field has no value.
    - **is not empty:** Triggers if the field has any value.
- **Value:** The specific value that triggers the logic.

> [!NOTE]
> The available operators change depending on the **type** of the target field. Number fields get mathematical operators (`>`, `<`, `>=`, `<=`), while text and select fields get string operators (`contains`, `not contains`).

## Operator Availability by Field Type

| Target Field Type | Available Operators |
| :--- | :--- |
| **Text / Textarea** | equals, not equals, contains, not contains, is empty, is not empty |
| **Number** | equals, not equals, greater than, less than, greater than or equals, less than or equals, is empty, is not empty |
| **Select / Radio / Checkbox** | equals, not equals, contains, not contains, is empty, is not empty |
| **Single Checkbox** | equals, not equals, is empty, is not empty |

## Practical Examples

### Example 1: Show a Text Field Based on a Checkbox
**Scenario:** You want to show an "Engraving Text" input only when the customer checks "Add Engraving?"

| Setting | Value |
| :--- | :--- |
| Action | **Show** |
| Match | **ALL** |
| Target Field | "Add Engraving?" (single_checkbox) |
| Operator | **equals** |
| Value | `1` |

### Example 2: Hide a Field Based on a Dropdown Selection
**Scenario:** You want to hide a "Custom Size" number field when the customer selects "Standard" from a size dropdown.

| Setting | Value |
| :--- | :--- |
| Action | **Hide** |
| Match | **ALL** |
| Target Field | "Size" (select) |
| Operator | **equals** |
| Value | `standard` |

### Example 3: Show a Field When ANY of Multiple Conditions Are Met
**Scenario:** You want to show a "Special Instructions" textarea when the customer selects either "Custom" from a type dropdown OR enters a number greater than 10 in a quantity field.

| Setting | Value |
| :--- | :--- |
| Action | **Show** |
| Match | **ANY** |
| Rule 1 | Target: "Type" → Operator: **equals** → Value: `custom` |
| Rule 2 | Target: "Quantity" → Operator: **greater than** → Value: `10` |

## Important Notes

> [!WARNING]
> Conditional logic only works between fields **within the same Option Group**. You cannot create rules that reference fields from a different group.

- **Frontend Behavior:** Conditions are evaluated instantly in the browser using JavaScript. There is no page reload — fields appear and disappear smoothly as the customer interacts with the form.
- **Hidden Field Values:** When a field is hidden by conditional logic, its value is **not submitted** with the form. This means hidden fields do not affect pricing or validation.
- **Multiple Rules:** You can add as many rules as you need by clicking the **+ Add Rule** button.

## Next Steps
- [Learn about Frontend Display](./frontend-display)
- [Explore Field Types](./builder)
