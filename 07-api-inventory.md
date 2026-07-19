# API Inventory

| Endpoint | Method | Authentication | Request | Response | Module | Purpose | Source |
| --- | --- | --- | --- | --- | --- | --- | --- |
| /capturePayment | ANY | No permission requirement declared | HTTP request parameters/body not formally documented in route. | RedirectResponse | drupal_commerce_razorpay | Payment/Razorpay endpoint. | modules/custom/drupal_commerce_razorpay/drupal_commerce_razorpay.routing.yml |
| /payment/ipn-handler | POST | CSRF token requirement | HTTP POST; body details inferred from controller source where available. | No explicit response returned | drupal_commerce_razorpay | Payment/Razorpay endpoint. | modules/custom/drupal_commerce_razorpay/drupal_commerce_razorpay.routing.yml |
| /generate-otp | POST | No permission requirement declared | HTTP POST; body details inferred from controller source where available. | JsonResponse | mobile_verify | OTP generation endpoint. | modules/custom/mobile_verify/mobile_verify.routing.yml |
| /generate-otp | POST | No permission requirement declared | HTTP POST; body details inferred from controller source where available. | JsonResponse | simple_login | OTP generation endpoint. | modules/custom/simple_login/simple_login.routing.yml |
