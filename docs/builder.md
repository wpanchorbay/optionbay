# Addon Builder

The **Addon Builder** is the heart of OptionBay. It's a powerful, drag-and-drop React interface that allows you to build complex product customization forms with ease.

## Interface Overview

When you edit an Option Group, you are presented with the Builder interface.

1. **Toolbar:** Contains the **Add Field** button and the **Save** controls.
2. **Field List:** Your current fields, which you can drag to reorder.
3. **Settings Panel:** Appears when you click on a field to edit its specific configuration.

## Available Field Types

OptionBay supports a wide range of input types to cover every use case:

| Field Type | Best For... |
| :--- | :--- |
| **[Text](./fields/text)** | Single line inputs like names or short messages. |
| **[Textarea](./fields/textarea)** | Longer messages like "Gift Note" or "Special Instructions". |
| **[Number](./fields/number)** | Quantities, dimensions, or any numeric data. |
| **[Select](./fields/select)** | Dropdown lists for choosing one item from many. |
| **[Radio](./fields/radio)** | Choosing one option where all choices are visible. |
| **[Checkbox](./fields/checkbox)** | Selecting multiple items from a list. |
| **[Single Checkbox](./fields/single-checkbox)** | A simple toggle (Yes/No) for things like "Add Warranty". |
| **[Image Swatches](./fields/image-swatch)** | Choosing between patterns, materials, or styles visually. |
| **[Color Swatches](./fields/color-swatch)** | Selecting colors from a palette. |
| **[File Upload](./fields/file-upload)** | Collecting logos, photos, or documents from customers. |
| **[Email](./fields/email)** | Capturing an email address for digital delivery or contact info. |


## Common Field Settings

Every field has a set of common attributes you can configure:

### General Settings
- **Label:** The title of the field shown to the customer.
- **Description:** Helpful instructions shown below the input.
- **Required:** If checked, the customer must fill this field before they can add the product to their cart.

### Pricing & Weight Settings
You can attach costs and physical weight to almost any field:
- **Price Type:** 
    - **Flat Fee:** A fixed cost.
    - **Percentage Increase:** Adds a percentage of the base product price.
    - **Character Count:** Cost multiplied by the number of characters typed (for text fields).
    - **Formula:** Advanced math-based pricing.
- **Price:** The numeric amount to add to the product total.
- **Formula:** (Only for Formula type) Use placeholders like `[char_count]`, `[base_price]`, `[quantity]`, or `[value]` to build complex calculations.
- **Weight:** The amount of physical weight to add to the product (affects shipping calculations).

### Appearance
- **Placeholder:** Ghost text shown inside the input (available for Text, Textarea, and Number fields).

## Reordering Fields
To change the order in which fields appear on the product page, simply grab the handle on the left of any field in the builder list and drag it to your preferred position.

## Next Steps
- [Setting up Conditional Logic](./conditional-logic)
- [Managing Product Assignments](./assignments)
