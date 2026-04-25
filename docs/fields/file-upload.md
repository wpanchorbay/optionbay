# File Upload Field

The **File Upload** field allows customers to attach files (images, documents, etc.) to their order. OptionBay handles the upload via the WordPress media system and validates the file against your configured restrictions during server-side processing.

## Common Use Cases
- Uploading a custom logo for printing on merchandise
- Attaching a reference photo for a custom illustration
- Submitting a PDF document (e.g., a resume for a printing service)
- Uploading a design file for laser engraving or 3D printing

## Field Settings

When you add a File Upload field and expand it in the builder, the following settings are available:

### General
| Setting | Description |
| :--- | :--- |
| **Label** | The title displayed above the upload area (e.g., "Upload Your Logo"). |
| **Description** | Optional help text shown below the field (e.g., "Accepted formats: JPG, PNG. Max 5MB."). |
| **Required** | When checked, the customer must upload a file before adding the product to the cart. |

### Pricing
Since the File Upload is not an options-based field, pricing is configured at the **field level**:

| Setting | Description |
| :--- | :--- |
| **Price Type** | Choose how the field affects the product price. Available types: **No Price**, **Flat Fee**, **Percentage of Base**, or **Formula**. |
| **Price Amount** | The numeric value to add when a file is uploaded. For example, charge a flat $10 fee for logo customization. |

### File Restrictions
| Setting | Description |
| :--- | :--- |
| **Allowed Extensions** | A comma-separated list of permitted file extensions (e.g., `.jpg,.png,.pdf,.svg`). If left empty, all common file types are accepted. |
| **Max File Size (MB)** | The maximum allowed file size in megabytes. Files exceeding this limit will be rejected during validation. Defaults to `5` MB. |

> [!WARNING]
> Make sure your server's `upload_max_filesize` and `post_max_size` PHP settings are at least as large as the Max File Size you configure here. Otherwise, PHP itself will reject the upload before OptionBay can process it.

## Conditional Logic
You can show or hide this field based on the value of another field in the same group. For example, show a "Upload Your Logo" field only when the customer selects "Custom Print" from a dropdown.

For full details on setting up rules, see the [Conditional Logic](../conditional-logic) page.
