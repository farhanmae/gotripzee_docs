# Folder Structure

| Path | Purpose |
| --- | --- |
| composer.json / composer.lock | Drupal project dependencies, scaffold settings, Composer patches. |
| autoload.php | Composer/Drupal autoload entry point. |
| config/sync | Drupal configuration export (1074 files). |
| modules/custom | Custom modules (8). |
| themes/custom/tripzee | Custom Tripzee front-end theme. |
| libraries | Vendored front-end libraries such as Colorbox, Flexslider, Litepicker, Splide, Fonticonpicker. |
| patches | Local Composer patch files. |
| docs | Generated inventory documentation. |

## Custom Module Files
| Module | Files |
| --- | --- |
| cab_booking | 5 |
| drupal_commerce_razorpay | 11 |
| mobile_verify | 8 |
| multiple_dates | 10 |
| package_booking | 4 |
| room_booking | 4 |
| simple_login | 7 |
| weekend_trip_booking | 3 |

## Config Export Families
| Family | Count |
| --- | --- |
| field.field | 204 |
| field.storage | 129 |
| core.entity_view_display | 100 |
| block.block | 63 |
| views.view | 63 |
| core.entity_form_display | 62 |
| system.action | 47 |
| core.entity_view_mode | 43 |
| webform.webform_options | 33 |
| simple_sitemap_engines.bundle_settings | 19 |
| image.style | 15 |
| core.date_format | 12 |
| pathauto.pattern | 11 |
| paragraphs.paragraphs_type | 10 |
| captcha.captcha_point | 9 |
| entityqueue.entity_queue | 9 |
| simple_sitemap.bundle_settings | 9 |
| flexslider.optionset | 8 |
| metatag.metatag_defaults | 8 |
| system.menu | 8 |
| taxonomy.vocabulary | 7 |
| commerce_product.commerce_product_type | 6 |
| commerce_product.commerce_product_variation_type | 6 |
| core.base_field_override | 6 |
| core.entity_form_mode | 6 |
| filter.format | 6 |
| node.type | 6 |
| simple_sitemap_engines.simple_sitemap_engine | 6 |
| block_content.type | 5 |
| commerce_order.commerce_order_item_type | 5 |
| media.type | 5 |
| splide.optionset | 4 |
| user.role | 4 |
| webform.webform | 4 |
| editor.editor | 3 |
| search.page | 3 |
| slick.optionset | 3 |
| commerce_payment.commerce_payment_gateway | 2 |
| commerce_product.commerce_product_attribute | 2 |
| contact.form | 2 |
| paragraphs_ee.paragraphs_category | 2 |
| simple_sitemap.sitemap | 2 |
| simple_sitemap.type | 2 |
| stringoverrides.string_override | 2 |
| system.image | 2 |
| system.theme | 2 |
| views_pdf.views_pdf_template | 2 |
| .htaccess | 1 |
| admin_toolbar.settings | 1 |
| admin_toolbar_tools.settings | 1 |
| automated_cron.settings | 1 |
| blazy.settings | 1 |
| bootstrap5.settings | 1 |
| captcha.settings | 1 |
| ckeditor_accordion.settings | 1 |
| claro.settings | 1 |
| colorbox.settings | 1 |
| comment.settings | 1 |
| comment.type | 1 |
| commerce_add_to_cart_link.settings | 1 |
| commerce_cart_redirection.settings | 1 |
| commerce_checkout.commerce_checkout_flow | 1 |
| commerce_email.commerce_email | 1 |
| commerce_number_pattern.commerce_number_pattern | 1 |
| commerce_order.commerce_order_type | 1 |
| commerce_order.settings | 1 |
| commerce_price.commerce_currency | 1 |
| commerce_stock.core_stock_events | 1 |
| commerce_stock.service_manager | 1 |
| commerce_stock_enforcement.settings | 1 |
| commerce_stock_local.commerce_stock_location_type | 1 |
| commerce_stock_local.cron | 1 |
| commerce_stock_local.transactions | 1 |
| commerce_store.commerce_store_type | 1 |
| contact.settings | 1 |
| core.extension | 1 |
| core.menu | 1 |
| dblog.settings | 1 |
| devel.settings | 1 |
| devel.toolbar | 1 |
