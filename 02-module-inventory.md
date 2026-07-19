# Module Inventory


## Cab Booking (`cab_booking`)
- Path: `modules/custom/cab_booking`
- Description: Custom module to simplify the cab booking.
- Core requirement: ^10
- Dependencies: None declared in info.yml
- Purpose: Custom module to simplify the cab booking.
- Entry points: `modules/custom/cab_booking/cab_booking.module`, `modules/custom/cab_booking/cab_booking.libraries.yml`
- Services: No custom services.yml found
- Routes: None
- Permissions: No custom permissions file found
- Hooks/functions: `cab_booking_form_commerce_order_item_add_to_cart_form_alter` (modules/custom/cab_booking/cab_booking.module:25), `cab_booking_availability_check` (modules/custom/cab_booking/cab_booking.module:62), `getDatesBetween` (modules/custom/cab_booking/cab_booking.module:198), `cab_booking_commerce_order_item_presave` (modules/custom/cab_booking/cab_booking.module:217), `cab_booking_availability_check_submit` (modules/custom/cab_booking/cab_booking.module:236)
- APIs used: Drupal Commerce Product/Order APIs, Form API
- APIs exposed: None


## Commerce Razorpay (`drupal_commerce_razorpay`)
- Path: `modules/custom/drupal_commerce_razorpay`
- Description: Provides Commerce integration for the Razorpay Payments.
- Core requirement: ^10
- Dependencies: `commerce_payment`
- Purpose: Provides Commerce integration for the Razorpay Payments.
- Entry points: `modules/custom/drupal_commerce_razorpay/drupal_commerce_razorpay.routing.yml`, `modules/custom/drupal_commerce_razorpay/drupal_commerce_razorpay.libraries.yml`
- Services: No custom services.yml found
- Routes: `drupal_commerce_razorpay.capturePayment` (/capturePayment), `drupal_commerce_razorpay.ipn_handler` (/payment/ipn-handler)
- Permissions: No custom permissions file found
- Hooks/functions: None found
- APIs used: Razorpay PHP SDK, Drupal Commerce Payment API
- APIs exposed: `/capturePayment`, `/payment/ipn-handler`


## Mobile Number Verification (`mobile_verify`)
- Path: `modules/custom/mobile_verify`
- Description: Verifiy mobile number on user registration using a system-generated OTP.
- Core requirement: ^8 || ^9 || ^10
- Dependencies: None declared in info.yml
- Purpose: Verifiy mobile number on user registration using a system-generated OTP.
- Entry points: `modules/custom/mobile_verify/mobile_verify.module`, `modules/custom/mobile_verify/mobile_verify.routing.yml`, `modules/custom/mobile_verify/mobile_verify.libraries.yml`
- Services: No custom services.yml found
- Routes: `mobile_verify.generate_otp` (/generate-otp)
- Permissions: No custom permissions file found
- Hooks/functions: `mobile_verify_form_alter` (modules/custom/mobile_verify/mobile_verify.module:8)
- APIs used: Textlocal SMS API, Drupal User API
- APIs exposed: `/generate-otp`


## Multiple Dates (`multiple_dates`)
- Path: `modules/custom/multiple_dates`
- Description: Multiple Dates form element using the jQuery UI datetimepicker.
- Core requirement: ^8 || ^9 || ^10
- Dependencies: `field`, `jquery_ui_datepicker`
- Purpose: Multiple Dates form element using the jQuery UI datetimepicker.
- Entry points: `modules/custom/multiple_dates/multiple_dates.module`, `modules/custom/multiple_dates/multiple_dates.libraries.yml`
- Services: No custom services.yml found
- Routes: None
- Permissions: No custom permissions file found
- Hooks/functions: `multiple_dates_help` (modules/custom/multiple_dates/multiple_dates.module:14), `multiple_dates_theme` (modules/custom/multiple_dates/multiple_dates.module:37), `get_formatted_date` (modules/custom/multiple_dates/multiple_dates.module:54)
- APIs used: Drupal APIs inferred from code
- APIs exposed: None


## Package Booking (`package_booking`)
- Path: `modules/custom/package_booking`
- Description: Custom module to check unavailability of packages based on selected dates.
- Core requirement: ^10
- Dependencies: None declared in info.yml
- Purpose: Custom module to check unavailability of packages based on selected dates.
- Entry points: `modules/custom/package_booking/package_booking.module`, `modules/custom/package_booking/package_booking.libraries.yml`
- Services: No custom services.yml found
- Routes: None
- Permissions: No custom permissions file found
- Hooks/functions: `package_booking_form_commerce_order_item_add_to_cart_form_alter` (modules/custom/package_booking/package_booking.module:26), `package_booking_availability_check` (modules/custom/package_booking/package_booking.module:63), `package_booking_availability_check_submit` (modules/custom/package_booking/package_booking.module:117)
- APIs used: Drupal Commerce Product/Order APIs, Form API
- APIs exposed: None


## Room Booking (`room_booking`)
- Path: `modules/custom/room_booking`
- Description: Custom module to simplify the room booking.
- Core requirement: ^10
- Dependencies: None declared in info.yml
- Purpose: Custom module to simplify the room booking.
- Entry points: `modules/custom/room_booking/room_booking.module`, `modules/custom/room_booking/room_booking.libraries.yml`
- Services: No custom services.yml found
- Routes: None
- Permissions: No custom permissions file found
- Hooks/functions: `room_booking_form_commerce_order_item_pado_add_to_cart_form_alter` (modules/custom/room_booking/room_booking.module:25), `room_booking_availability_check` (modules/custom/room_booking/room_booking.module:61), `getDatesBetweenRoom` (modules/custom/room_booking/room_booking.module:197), `room_booking_commerce_order_item_presave` (modules/custom/room_booking/room_booking.module:216), `room_booking_availability_check_submit` (modules/custom/room_booking/room_booking.module:235)
- APIs used: Drupal Commerce Product/Order APIs, Form API
- APIs exposed: None


## Simple Login (`simple_login`)
- Path: `modules/custom/simple_login`
- Description: Allows users to log in using a system-generated OTP code instead of a password.
- Core requirement: ^8 || ^9 || ^10
- Dependencies: None declared in info.yml
- Purpose: Allows users to log in using a system-generated OTP code instead of a password.
- Entry points: `modules/custom/simple_login/simple_login.module`, `modules/custom/simple_login/simple_login.routing.yml`, `modules/custom/simple_login/simple_login.libraries.yml`
- Services: No custom services.yml found
- Routes: `simple_login.generate_otp` (/generate-otp)
- Permissions: No custom permissions file found
- Hooks/functions: `simple_login_form_alter` (modules/custom/simple_login/simple_login.module:8), `simple_login_user_logout` (modules/custom/simple_login/simple_login.module:22)
- APIs used: Textlocal SMS API, Drupal User API
- APIs exposed: `/generate-otp`


## Weekend Trip Booking (`weekend_trip_booking`)
- Path: `modules/custom/weekend_trip_booking`
- Description: Custom module to simplify the weekend trip booking.
- Core requirement: ^10
- Dependencies: None declared in info.yml
- Purpose: Custom module to simplify the weekend trip booking.
- Entry points: `modules/custom/weekend_trip_booking/weekend_trip_booking.module`, `modules/custom/weekend_trip_booking/weekend_trip_booking.libraries.yml`
- Services: No custom services.yml found
- Routes: None
- Permissions: No custom permissions file found
- Hooks/functions: `weekend_trip_booking_form_commerce_order_item_add_to_cart_form_alter` (modules/custom/weekend_trip_booking/weekend_trip_booking.module:25), `weekend_trip_booking_availability_check` (modules/custom/weekend_trip_booking/weekend_trip_booking.module:61), `weekend_trip_booking_availability_check_submit` (modules/custom/weekend_trip_booking/weekend_trip_booking.module:166)
- APIs used: Drupal Commerce Product/Order APIs, Form API
- APIs exposed: None
