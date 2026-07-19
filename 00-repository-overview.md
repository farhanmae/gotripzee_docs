# Repository Overview

## Confirmed Purpose
GoTripzee is a Drupal Commerce travel booking site. Static inspection confirms Commerce product bundles for cabs, stays/rooms, packages, events/trips, and weekend trips; custom add-to-cart availability modules; OTP login/mobile verification endpoints; Razorpay payment integration; Webform lead/contact forms; Views-based listings; and a custom Bootstrap 5 child theme named Tripzee.

## Architecture
- Drupal recommended-project with document root at repository root, configured by `composer.json` `extra.drupal-scaffold.locations.web-root: ./`.
- Custom modules live in `modules/custom`.
- The custom front-end theme lives in `themes/custom/tripzee` and extends `bootstrap5`.
- Site configuration export lives in `config/sync` with 1074 YAML files.
- Third-party browser libraries are vendored in `libraries`.

## Technology Stack
- Drupal 10
- Drupal Commerce 2.x
- PHP packages via Composer
- Twig
- jQuery/Drupal behaviors
- Bootstrap 5 theme base
- Razorpay
- Textlocal SMS
- Search API database backend
- Webform
- Views

## Major Composer Dependencies
| Package | Version |
| --- | --- |
| composer/installers | ^2.0 |
| cweagans/composer-patches | ^1.7 |
| drupal/admin_toolbar | ^3.4 |
| drupal/bat | ^11.0 |
| drupal/bee_hotel | 2.21.0 |
| drupal/best_selling_products | ^3.13 |
| drupal/blazy | ^3.0 |
| drupal/bootstrap5 | ^3.0 |
| drupal/ckeditor5_icons | ^1.0@RC |
| drupal/ckeditor_accordion | ^2.2 |
| drupal/colorbox | ^2.0 |
| drupal/colorbox_inline | ^2.0 |
| drupal/colorbox_media_video | ^2.0 |
| drupal/commerce | ^2.38 |
| drupal/commerce_add_to_cart_link | ^2.0 |
| drupal/commerce_autosku | ^2.1 |
| drupal/commerce_bulk | ^2.0@beta |
| drupal/commerce_buy_now | ^1.0@RC |
| drupal/commerce_cart_redirection | ^3.2 |
| drupal/commerce_checkout_order_fields | ^1.2 |
| drupal/commerce_email | ^1.3 |
| drupal/commerce_invoice | ^2.0@RC |
| drupal/commerce_pado | ^1.3 |
| drupal/commerce_partial_payments | ^3.0 |
| drupal/commerce_pricelist | ^2.10 |
| drupal/commerce_product_limits | ^1.0 |
| drupal/commerce_stock | ^1.3 |
| drupal/content_planner | ^1.1 |
| drupal/core-composer-scaffold | ^10.2 |
| drupal/core-project-message | ^10.2 |
| drupal/core-recommended | ^10.2 |
| drupal/ctools | ^4.1 |
| drupal/date_filter | ^1.0 |
| drupal/devel | ^5.1 |
| drupal/dynamic_entity_reference | ^3.2 |
| drupal/entity_clone | ^2.0@beta |
| drupal/entity_print | ^2.14 |
| drupal/entityqueue | ^1.9 |
| drupal/field_group | ^4.0 |
| drupal/fivestar | ^1.0@alpha |
| drupal/flexslider | ^3.0@alpha |
| drupal/fontawesome | ^2.26 |
| drupal/fullcalendar_library | ^3.0 |
| drupal/gin | ^3.0@RC |
| drupal/gin_toolbar | ^1.0@rc |
| drupal/google_map_field | ^2.0 |
| drupal/google_tag | ^2.0 |
| drupal/hook_event_dispatcher | ^4.0@RC |
| drupal/jquery_ui_datepicker | ^2.0 |
| drupal/mailsystem | ^4.4 |
| drupal/masquerade | ^2.0 |
| drupal/menu_item_role_access | ^2.1 |
| drupal/menu_link_attributes | ^1.3 |
| drupal/metatag | ^2.1 |
| drupal/node_read_time | ^1.15 |
| drupal/office_hours | ^1.21 |
| drupal/otp_field | ^1.0@beta |
| drupal/pages_restriction | ^2.0 |
| drupal/paragraphs_ee | ^10.0 |
| drupal/paragraphs_features | ^2.0@beta |
| drupal/paragraphs_jquery_ui_accordion | ^1.6 |
| drupal/password_eye | ^2.1 |
| drupal/pathauto | ^1.12 |
| drupal/phone_number | ^2.0@alpha |
| drupal/profile | ^1.10 |
| drupal/range_slider | ^2.1 |
| drupal/recaptcha_v3 | ^2.0 |
| drupal/redirect | ^1.9 |
| drupal/rules | ^4.0 |
| drupal/search_api | ^1.34 |
| drupal/show_email | ^1.2 |
| drupal/simple_pass_reset | ^1.2 |
| drupal/simple_sitemap | ^4.2 |
| drupal/simpleautologout | ^2.0 |
| drupal/slick | ^3.0 |
| drupal/slick_extras | ^2.0 |
| drupal/slick_lightbox | ^2.0 |
| drupal/slick_views | ^3.0 |
| drupal/sms_fast2sms | ^1.0@alpha |
| drupal/smsframework | ^2.2@RC |
| drupal/smtp | ^1.2 |
| drupal/splide | ^2.0 |
| drupal/splidebox | ^2.0 |
| drupal/stringoverrides | ^1.8 |
| drupal/symfony_mailer | ^1.4 |
| drupal/terms_of_use | ^2.4 |
| drupal/token | ^1.14 |
| drupal/twig_tweak | ^3.2 |
| drupal/typed_data | ^2.1 |
| drupal/video | ^3.0 |
| drupal/views_accordion | ^2.0 |
| drupal/views_autocomplete_filters | ^2.0 |
| drupal/views_conditional | ^1.9 |
| drupal/views_field_view | ^1.0@beta |
| drupal/views_pdf | ^3.0@alpha |
| drupal/webform | ^6.2 |
| drupal/webform_views | ^5.2 |
| drush/drush | ^13.3 |
| mikehaertl/phpwkhtmltopdf | ~2.1 |
| razorpay/razorpay | ^2.9 |
| roomify/bat | ^1.4 |
| tecnickcom/tcpdf | ~6 |

## Build And Deployment
- Composer is the confirmed PHP dependency/build mechanism.
- Drupal scaffold installs web assets into the repository root.
- No Dockerfile, CI workflow, or shell deployment script was confirmed in the inspected non-vendor files.
- Composer patches are declared for Drupal core and several contributed modules in `composer.json`.
