# Service Inventory

## Registered Custom Services
No custom `*.services.yml` files were found under `modules/custom`; therefore no registered custom Drupal services were confirmed.

## Service-Like Classes / Plugins
| Class | File | Responsibilities | Methods | Consumers |
| --- | --- | --- | --- | --- |
| Drupal\drupal_commerce_razorpay\AutoWebhook | modules/custom/drupal_commerce_razorpay/src/AutoWebhook.php:8 | Creates/updates Razorpay webhooks and stores webhook flags in config. | generateWebhookSecret, autoEnableWebhook | Commerce payment gateway/forms/routes |
| Drupal\drupal_commerce_razorpay\PluginForm\RazorpayForm | modules/custom/drupal_commerce_razorpay/src/PluginForm/RazorpayForm.php:16 | Utility/class discovered by static PHP scan. | createOrGetRazorpayOrderId, getRazorpayApiInstance, setPaymentConfigAndMessenger, generateCheckoutForm, buildConfigurationForm | Commerce payment gateway/forms/routes |
| to | themes/custom/tripzee/tripzee.theme:7 | Utility/class discovered by static PHP scan. |  | Drupal plugin manager or procedural hook code |
| to | themes/custom/tripzee/tripzee.theme:7 | Utility/class discovered by static PHP scan. |  | Drupal plugin manager or procedural hook code |
| Drupal\drupal_commerce_razorpay\Plugin\Commerce\PaymentGateway\RazorpayCheckout | modules/custom/drupal_commerce_razorpay/src/Plugin/Commerce/PaymentGateway/RazorpayCheckout.php:32 | Drupal plugin class. | defaultConfiguration, buildConfigurationForm, validateConfigurationForm, submitConfigurationForm, onReturn, capturePayment, voidPayment, refundPayment, getRazorpayApiInstance, onCancel, onNotify | Commerce payment gateway/forms/routes |
| Drupal\drupal_commerce_razorpay\Plugin\Commerce\PaymentGateway\RazorpayInterface | modules/custom/drupal_commerce_razorpay/src/Plugin/Commerce/PaymentGateway/RazorpayInterface.php | Drupal plugin class. |  | Commerce payment gateway/forms/routes |
| Drupal\multiple_dates\Plugin\Field\FieldFormatter\MultipleDatesDefaultFormatter | modules/custom/multiple_dates/src/Plugin/Field/FieldFormatter/MultipleDatesDefaultFormatter.php:24 | Drupal plugin class. | settingsForm, settingsSummary, viewElements | Drupal plugin manager or procedural hook code |
| Drupal\multiple_dates\Plugin\Field\FieldType\MultipleDatesFieldItem | modules/custom/multiple_dates/src/Plugin/Field/FieldType/MultipleDatesFieldItem.php:23 | Drupal plugin class. | isEmpty | Drupal plugin manager or procedural hook code |
| Drupal\multiple_dates\Plugin\Field\FieldWidget\MultipleDatesDefaultWidget | modules/custom/multiple_dates/src/Plugin/Field/FieldWidget/MultipleDatesDefaultWidget.php:23 | Drupal plugin class. | formElement, settingsForm, settingsSummary, validate | Drupal plugin manager or procedural hook code |
