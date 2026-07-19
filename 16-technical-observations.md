# Technical Observations

## Confirmed Findings
- No custom services.yml files were found under modules/custom.
- No custom tests were found under modules/custom or themes/custom.
- Custom booking modules use hook_form_alter and hook_commerce_order_item_presave style procedural code.
- Razorpay integration includes a Commerce payment gateway plugin plus custom /capturePayment and /payment/ipn-handler routes.
- simple_login and mobile_verify both declare /generate-otp POST routes, creating a route path collision at the URL level.

## Potential Issues Observed
- Potential hardcoded/security-sensitive usage: key_secret in modules/custom/drupal_commerce_razorpay/src/AutoWebhook.php:29.
- Potential hardcoded/security-sensitive usage: secret in modules/custom/drupal_commerce_razorpay/src/AutoWebhook.php:29.
- Potential hardcoded/security-sensitive usage: key_secret in modules/custom/drupal_commerce_razorpay/src/Plugin/Commerce/PaymentGateway/RazorpayCheckout.php:57.
- Potential hardcoded/security-sensitive usage: secret in modules/custom/drupal_commerce_razorpay/src/Plugin/Commerce/PaymentGateway/RazorpayCheckout.php:57.
- Potential hardcoded/security-sensitive usage: key_secret in modules/custom/drupal_commerce_razorpay/src/PluginForm/RazorpayForm.php:162.
- Potential hardcoded/security-sensitive usage: secret in modules/custom/drupal_commerce_razorpay/src/PluginForm/RazorpayForm.php:156.
- Potential hardcoded/security-sensitive usage: apiKey in modules/custom/mobile_verify/src/Controller/MobileVerifyController.php:27.
- Potential hardcoded/security-sensitive usage: apikey in modules/custom/mobile_verify/src/Controller/MobileVerifyController.php:38.
- Potential hardcoded/security-sensitive usage: curl_init in modules/custom/mobile_verify/src/Controller/MobileVerifyController.php:41.
- Potential hardcoded/security-sensitive usage: apiKey in modules/custom/simple_login/src/Controller/SimpleLoginController.php:47.
- Potential hardcoded/security-sensitive usage: apikey in modules/custom/simple_login/src/Controller/SimpleLoginController.php:58.
- Potential hardcoded/security-sensitive usage: curl_init in modules/custom/simple_login/src/Controller/SimpleLoginController.php:61.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--article.html.twig:95.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--destination.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--about.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--admin-dashboard.html.twig:89.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--cabs.html.twig:131.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--contact-us.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--events.html.twig:96.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--faqs.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--packages-regions.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--packages.html.twig:101.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--stays.html.twig:100.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--team.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--page--weekend-trips.html.twig:95.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--team.html.twig:106.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node--testimonial.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/content/node.html.twig:94.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/includes/header.html.twig:15.
- Potential hardcoded/security-sensitive usage: _access in themes/custom/tripzee/templates/layout/page--user--register.html.twig:15.
- Booking availability checks call loadMultiple() on commerce_order storage and then iterate all completed orders; this is a potential performance hotspot on large order volumes.
- Several routes declare _access TRUE or only CSRF token requirements; access posture should be reviewed against intended exposure.
- OTP login resets user passwords to numeric OTPs and logs generated OTP values.
- cab_booking_old.module contains older duplicate cab booking logic and dpm() debug usage.

## Dead Code / Duplicate Logic
- `modules/custom/cab_booking/cab_booking_old.module` contains older cab booking logic and duplicate function names relative to `cab_booking.module`. Because the filename is not `cab_booking.module`, it is not a standard Drupal module entry point, but it remains in the repository.
- Cab and room booking modules contain near-identical availability and quantity logic with bundle/field differences.
- Simple login and mobile verify both expose `/generate-otp` with route name differences, which is a confirmed URL collision in static routing files.

## Security Concerns
- OTP values are logged by simple login code.
- OTP login resets the Drupal user password to the generated OTP.
- Textlocal API key literal is present in source.
- Some custom routes use `_access: TRUE`.
- Razorpay `/capturePayment` has an explicit TODO comment that access should be changed later.

## Performance Concerns
- Cab, room, and weekend trip booking validation load all commerce orders and iterate completed orders/items in PHP.
- Large Views configuration and Search API listings are central to catalog pages; runtime performance depends on index freshness and view query configuration.

## Assumptions
- Database tables for config entities and fields are inferred from Drupal entity/field storage conventions because no SQL dump or Drupal runtime schema inspection is present.
- Entity business purposes are inferred from bundle names, labels, fields, and templates.
