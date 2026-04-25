# Conditional Logic

**Conditional Logic** allows you to create dynamic forms that react to user input. You can show or hide specific fields based on the selections your customers make, creating a much cleaner and more professional shopping experience.

## How it Works

Every field in the Addon Builder can have its own set of "Conditional Rules." When these rules are met, the field will either **Show** or **Hide** automatically on the product page.

## Setting Up Rules

1. Open a field for editing in the **Addon Builder**.
2. Navigate to the **Logic** or **Conditions** tab in the field settings.
3. Click **Add Rule**.

### Rule Components
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

### Match Strategy
If you have multiple rules for a single field, you can choose how they interact:
- **ALL:** Every single rule must be true for the action to trigger.
- **ANY:** If at least one rule is true, the action will trigger.

## Use Case Examples

### Example 1: Personalized Engraving
- **Field A:** Checkbox labeled "Add Custom Engraving?"
- **Field B:** Text field for "Engraving Text."
- **Logic:** Set Field B to **Show** only if Field A **Equals** "Yes".

### Example 2: Material-Specific Options
- **Field A:** Dropdown with "Wood", "Metal", and "Plastic".
- **Field B:** Dropdown with "Wood Stain Colors".
- **Logic:** Set Field B to **Show** only if Field A **Equals** "Wood".

## Performance & UX

OptionBay's logic engine runs instantly in the browser. When a field is hidden by logic:
1. It is removed from the price calculation.
2. Its value is cleared (so it doesn't get submitted with the order).
3. The "Add to Cart" validation ignores it.

## Best Practices

- **Avoid Infinite Loops:** Be careful not to create rules where Field A depends on Field B, and Field B depends on Field A.
- **Keep it Simple:** Start with simple "Show" rules. Complex "Hide" rules can sometimes be confusing to manage as your form grows.
- **Test Thoroughly:** Always preview your product page to ensure the logic flows naturally for the shopper.
