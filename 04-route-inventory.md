# Route Inventory

| Route | URL | Controller | Method | Requirement | Module | Parameters | Source |
| --- | --- | --- | --- | --- | --- | --- | --- |
| drupal_commerce_razorpay.capturePayment | /capturePayment | \Drupal\drupal_commerce_razorpay\Controller\RzpController::capturePayment | ANY | _access: TRUE | drupal_commerce_razorpay |  | modules/custom/drupal_commerce_razorpay/drupal_commerce_razorpay.routing.yml:1 |
| drupal_commerce_razorpay.ipn_handler | /payment/ipn-handler | \Drupal\drupal_commerce_razorpay\Controller\IPNController::handleIPN | POST | _csrf_token: TRUE | drupal_commerce_razorpay |  | modules/custom/drupal_commerce_razorpay/drupal_commerce_razorpay.routing.yml:9 |
| mobile_verify.generate_otp | /generate-otp | \Drupal\mobile_verify\Controller\MobileVerifyController::processLogin | POST | _access: TRUE | mobile_verify |  | modules/custom/mobile_verify/mobile_verify.routing.yml:1 |
| simple_login.generate_otp | /generate-otp | \Drupal\simple_login\Controller\SimpleLoginController::processLogin | POST | _access: TRUE | simple_login |  | modules/custom/simple_login/simple_login.routing.yml:1 |
