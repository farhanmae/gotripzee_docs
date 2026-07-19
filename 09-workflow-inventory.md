# Workflow Inventory

## Content Moderation / Workflows
| Workflow | Label | Type | States/Transitions Source | File |
| --- | --- | --- | --- | --- |
| editorial | Editorial | content_moderation | 8 parsed keys | config/sync/workflows.workflow.editorial.yml |

## Booking Workflows
- Cab booking: add-to-cart form is altered for `commerce_order_item_add_to_cart_form`; selected `field_date` ranges are checked against `field_unavailable_dates`, completed orders, and `field_availability`; quantity is set to number of booked days before checkout redirect.
- Room/stay booking: same pattern as cab booking, targeting `room` order items and product bundles.
- Package booking: add-to-cart form is altered for `package`; selected package type is validated against `attribute_package_type`; checkout redirect follows submit.
- Weekend trip booking: add-to-cart form is altered for `weekend_trip`; selected `field_booking_date` is compared with completed order items and `field_availability`; checkout redirect follows submit.

## Notifications And Background Jobs
- OTP endpoints send SMS through Textlocal via cURL.
- Razorpay webhook/IPN/payment notification support exists in custom payment gateway code.
- `automated_cron.settings.yml` interval is configured to 10800 seconds.
- Scheduler and Commerce Stock cron/settings config files are present.
