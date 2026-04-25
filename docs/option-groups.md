# Option Groups

**Option Groups** are the building blocks of OptionBay. Instead of creating options for every product individually, you create reusable "groups" that can be assigned to multiple products, categories, or tags. This modular approach saves time and ensures consistency across your store.

## Creating an Option Group

To create your first group:
1. Navigate to **Products > Options** in your WordPress dashboard.
2. Click the **Add New** button at the top.
3. Enter a **Title** for your group (e.g., "Gift Wrapping Options" or "Technical Specifications"). This title is for your internal reference and is not shown to customers.
4. Use the **[Addon Builder](./builder)** to add fields to your group.
5. Configure the **[Product Assignments](./assignments)** to decide where these options should appear.
6. Click **Save** to publish the group.

## Managing Your Groups

The main Options page provides an overview of all your created groups in a WordPress-style list table.

### Group Overview Table
| Column | Description |
| :--- | :--- |
| **Title** | The internal name of the group. Click to edit. |
| **Status** | Whether the group is currently **Published** (live on the store) or saved as a **Draft**. |

### Row Actions
When you hover over a group in the list, the following actions appear:

| Action | Description |
| :--- | :--- |
| **Edit** | Opens the Addon Builder for this group so you can modify fields, pricing, and logic. |
| **Duplicate** | Creates an exact copy of the group, including all fields, options, pricing, and assignment rules. Useful for creating variations of complex sets. |
| **Delete** | Permanently removes the group and all its associated assignments. This action cannot be undone. |

## Group Status

Each group has a status that determines its visibility:

- **Published:** The group is live and will appear on products that match its assignment rules.
- **Draft:** The group is saved but will **not** be displayed on the frontend. Use this while you're still building or testing your options.

> [!TIP]
> Use the **Draft** status while building complex option groups with conditional logic. This way, you can save your work in progress without customers seeing unfinished options on your store.

## Best Practices

- **Keep it Modular:** Instead of one massive group with 50 fields, break them into smaller, focused groups (e.g., "Basic Personalization" and "Premium Addons"). This makes management easier and allows you to reuse individual groups across different products.
- **Clear Naming:** Use descriptive titles for your groups (e.g., "T-Shirt Customization" rather than "Group 1") so you can easily identify them when setting up assignment rules.
- **Test with Draft Mode:** Always preview your options by switching the group to "Published" on a test product before going live on your entire catalog.

## Next Steps
- [Learn how to use the Addon Builder](./builder)
- [Configure Product Assignments](./assignments)
