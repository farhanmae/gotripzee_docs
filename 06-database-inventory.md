# Database Inventory

## Confirmed Custom Schema
No custom `hook_schema()`, SQL migration files, or explicit custom database tables were found in `modules/custom`.

## Drupal-Managed Tables
Database storage is primarily Drupal-managed entity and Field API storage inferred from configuration exports. Examples:
- Node bundles use Drupal node tables plus field tables generated from `field.storage.node.*.yml`.
- Commerce product and variation bundles use Commerce entity tables plus field tables generated from `field.storage.commerce_product.*.yml` and `field.storage.commerce_product_variation.*.yml`.
- Commerce order item bundles use Commerce order item tables plus configured field storage.
- The `multiple_dates` module defines a custom Field API type with schema column `multiple_dates` in `modules/custom/multiple_dates/src/Plugin/Field/FieldType/MultipleDatesFieldItem.php`.

## Field Storage Summary
| Entity Type | Field Count |
| --- | --- |
| commerce_product | 46 |
| node | 18 |
| commerce_product_variation | 12 |
| commerce_order | 10 |
| block_content | 9 |
| user | 9 |
| paragraph | 7 |
| commerce_order_item | 5 |
| media | 5 |
| taxonomy_term | 4 |
| profile | 3 |
| comment | 1 |

## Custom Tables
| Table | PK | FK | Indexes/Constraints | Source |
| --- | --- | --- | --- | --- |
| Drupal Field API storage table generated for field type usage | Managed by Drupal Field API | Managed by Drupal Field API | Managed by Drupal Field API | modules/custom/multiple_dates/src/Plugin/Field/FieldType/MultipleDatesFieldItem.php |
