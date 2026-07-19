# Dependency Graph

## Module To Module
| Module | Dependencies |
| --- | --- |
| cab_booking |  |
| drupal_commerce_razorpay | commerce_payment |
| mobile_verify |  |
| multiple_dates | field, jquery_ui_datepicker |
| package_booking |  |
| room_booking |  |
| simple_login |  |
| weekend_trip_booking |  |

## Controller To API
| Controller | Route | Endpoint |
| --- | --- | --- |
| Drupal\drupal_commerce_razorpay\Controller\IPNController | drupal_commerce_razorpay.ipn_handler | /payment/ipn-handler |
| Drupal\drupal_commerce_razorpay\Controller\RzpController | drupal_commerce_razorpay.capturePayment | /capturePayment |
| Drupal\mobile_verify\Controller\MobileVerifyController | mobile_verify.generate_otp | /generate-otp |
| Drupal\simple_login\Controller\SimpleLoginController | simple_login.generate_otp | /generate-otp |

## Module To Entity Bundle
| Module | Bundles |
| --- | --- |
| cab_booking | commerce_product.cab, commerce_order_item.cab |
| room_booking | commerce_product.room, commerce_order_item.room |
| package_booking | commerce_product.package, commerce_product_variation.package |
| weekend_trip_booking | commerce_product.weekend_trip, commerce_order_item.weekend_trip |
| multiple_dates | commerce_product.cab, commerce_product.package, commerce_product.room, commerce_product.weekend_trip, commerce_product_variation.package |

## Graph Data
```json
{
  "module_to_module": [
    {
      "module": "cab_booking",
      "dependencies": []
    },
    {
      "module": "drupal_commerce_razorpay",
      "dependencies": [
        "commerce_payment"
      ]
    },
    {
      "module": "mobile_verify",
      "dependencies": []
    },
    {
      "module": "multiple_dates",
      "dependencies": [
        "field",
        "jquery_ui_datepicker"
      ]
    },
    {
      "module": "package_booking",
      "dependencies": []
    },
    {
      "module": "room_booking",
      "dependencies": []
    },
    {
      "module": "simple_login",
      "dependencies": []
    },
    {
      "module": "weekend_trip_booking",
      "dependencies": []
    }
  ],
  "controller_to_service": [
    {
      "controller": "Drupal\\drupal_commerce_razorpay\\Controller\\IPNController",
      "services": "No constructor/container injection detected"
    },
    {
      "controller": "Drupal\\drupal_commerce_razorpay\\Controller\\RzpController",
      "services": "No constructor/container injection detected"
    },
    {
      "controller": "Drupal\\mobile_verify\\Controller\\MobileVerifyController",
      "services": "No constructor/container injection detected"
    },
    {
      "controller": "Drupal\\simple_login\\Controller\\SimpleLoginController",
      "services": "No constructor/container injection detected"
    }
  ],
  "service_to_repository": [],
  "repository_to_database": [],
  "controller_to_api": [
    {
      "controller": "Drupal\\drupal_commerce_razorpay\\Controller\\IPNController",
      "route": "drupal_commerce_razorpay.ipn_handler",
      "endpoint": "/payment/ipn-handler"
    },
    {
      "controller": "Drupal\\drupal_commerce_razorpay\\Controller\\RzpController",
      "route": "drupal_commerce_razorpay.capturePayment",
      "endpoint": "/capturePayment"
    },
    {
      "controller": "Drupal\\mobile_verify\\Controller\\MobileVerifyController",
      "route": "mobile_verify.generate_otp",
      "endpoint": "/generate-otp"
    },
    {
      "controller": "Drupal\\simple_login\\Controller\\SimpleLoginController",
      "route": "simple_login.generate_otp",
      "endpoint": "/generate-otp"
    }
  ],
  "module_to_configuration": [
    {
      "module": "cab_booking",
      "config_files": []
    },
    {
      "module": "drupal_commerce_razorpay",
      "config_files": [
        "config/sync/drupal_commerce_razorpay.settings.yml"
      ]
    },
    {
      "module": "mobile_verify",
      "config_files": []
    },
    {
      "module": "multiple_dates",
      "config_files": []
    },
    {
      "module": "package_booking",
      "config_files": []
    },
    {
      "module": "room_booking",
      "config_files": []
    },
    {
      "module": "simple_login",
      "config_files": []
    },
    {
      "module": "weekend_trip_booking",
      "config_files": []
    }
  ],
  "module_to_entity_bundle": [
    {
      "module": "cab_booking",
      "bundles": [
        "commerce_product.cab",
        "commerce_order_item.cab"
      ]
    },
    {
      "module": "room_booking",
      "bundles": [
        "commerce_product.room",
        "commerce_order_item.room"
      ]
    },
    {
      "module": "package_booking",
      "bundles": [
        "commerce_product.package",
        "commerce_product_variation.package"
      ]
    },
    {
      "module": "weekend_trip_booking",
      "bundles": [
        "commerce_product.weekend_trip",
        "commerce_order_item.weekend_trip"
      ]
    },
    {
      "module": "multiple_dates",
      "bundles": [
        "commerce_product.cab",
        "commerce_product.package",
        "commerce_product.room",
        "commerce_product.weekend_trip",
        "commerce_product_variation.package"
      ]
    }
  ]
}
```
