# Entity Inventory


## block_content.basic (Basic block)
- Source: `config/sync/block_content.type.basic.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Body | text_with_summary | 1 | false | config/sync/field.field.block_content.basic.body.yml |


## block_content.basic_block_with_image (Basic Block with Image)
- Source: `config/sync/block_content.type.basic_block_with_image.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_image | Image | image | 1 | false | config/sync/field.field.block_content.basic_block_with_image.field_image.yml |
| field_secondary_text | Secondary Text | string_long | 1 | false | config/sync/field.field.block_content.basic_block_with_image.field_secondary_text.yml |
| field_title | Title | string_long | 1 | false | config/sync/field.field.block_content.basic_block_with_image.field_title.yml |


## block_content.cta_block (CTA Block)
- Source: `config/sync/block_content.type.cta_block.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_media`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_button | Button | link | 1 | false | config/sync/field.field.block_content.cta_block.field_button.yml |
| field_media | Image/Video | entity_reference | 1 | false | config/sync/field.field.block_content.cta_block.field_media.yml |
| field_secondary_text | Secondary Text | string_long | 1 | false | config/sync/field.field.block_content.cta_block.field_secondary_text.yml |
| field_title | Title | string_long | 1 | false | config/sync/field.field.block_content.cta_block.field_title.yml |


## block_content.image_block (Image Block)
- Source: `config/sync/block_content.type.image_block.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_featured_on | Featured On | boolean | 1 | false | config/sync/field.field.block_content.image_block.field_featured_on.yml |
| field_image | Image | image | 1 | false | config/sync/field.field.block_content.image_block.field_image.yml |
| field_link | Link | link | 1 | false | config/sync/field.field.block_content.image_block.field_link.yml |


## block_content.promo_block (Promo Block)
- Source: `config/sync/block_content.type.promo_block.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_image`, `field_mobile_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_button | Link | link | 1 | true | config/sync/field.field.block_content.promo_block.field_button.yml |
| field_image | Image | image | 1 | true | config/sync/field.field.block_content.promo_block.field_image.yml |
| field_mobile_image | Mobile Image | image | 1 | false | config/sync/field.field.block_content.promo_block.field_mobile_image.yml |


## commerce_order_item.cab (Cab)
- Source: `config/sync/commerce_order.commerce_order_item_type.cab.yml`
- Business purpose: Commerce order item type used by booking flows.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_date | Date | daterange | 1 | false | config/sync/field.field.commerce_order_item.cab.field_date.yml |


## commerce_order_item.default (Default)
- Source: `config/sync/commerce_order.commerce_order_item_type.default.yml`
- Business purpose: Commerce order item type used by booking flows.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_booking_date | Date of Arrival | datetime | 1 | true | config/sync/field.field.commerce_order_item.default.field_booking_date.yml |


## commerce_order_item.event (Event)
- Source: `config/sync/commerce_order.commerce_order_item_type.event.yml`
- Business purpose: Commerce order item type used by booking flows.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## commerce_order_item.room (Stay)
- Source: `config/sync/commerce_order.commerce_order_item_type.room.yml`
- Business purpose: Commerce order item type used by booking flows.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_adults | No. of Adults | integer | 1 | false | config/sync/field.field.commerce_order_item.room.field_adults.yml |
| field_bed | Extra Adult | boolean | 1 | false | config/sync/field.field.commerce_order_item.room.field_bed.yml |
| field_children | No. of Children | integer | 1 | false | config/sync/field.field.commerce_order_item.room.field_children.yml |
| field_date | Date | daterange | 1 | false | config/sync/field.field.commerce_order_item.room.field_date.yml |


## commerce_order_item.weekend_trip (Weekend Trip)
- Source: `config/sync/commerce_order.commerce_order_item_type.weekend_trip.yml`
- Business purpose: Commerce order item type used by booking flows.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_booking_date | Booking Date | datetime | 1 | true | config/sync/field.field.commerce_order_item.weekend_trip.field_booking_date.yml |


## commerce_product.cab (Cab)
- Source: `config/sync/commerce_product.commerce_product_type.cab.yml`
- Business purpose: Commerce product bundle for travel catalog/booking inventory.
- Relationships: `field_destinations`, `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Body | text_with_summary | 1 | false | config/sync/field.field.commerce_product.cab.body.yml |
| field_availability | Availability | integer | 1 | false | config/sync/field.field.commerce_product.cab.field_availability.yml |
| field_deposit_percentage | Deposit Percentage | integer | 1 | false | config/sync/field.field.commerce_product.cab.field_deposit_percentage.yml |
| field_destinations | Destinations | entity_reference | -1 | false | config/sync/field.field.commerce_product.cab.field_destinations.yml |
| field_disable_booking | Disable Booking | boolean | 1 | false | config/sync/field.field.commerce_product.cab.field_disable_booking.yml |
| field_image | Image | image | 1 | false | config/sync/field.field.commerce_product.cab.field_image.yml |
| field_key_points | Key Points | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.cab.field_key_points.yml |
| field_meta_tags | Meta Tags | metatag | 1 | false | config/sync/field.field.commerce_product.cab.field_meta_tags.yml |
| field_seating_capacity | Seating Capacity | integer | 1 | false | config/sync/field.field.commerce_product.cab.field_seating_capacity.yml |
| field_sold_out | Sold Out | boolean | 1 | false | config/sync/field.field.commerce_product.cab.field_sold_out.yml |
| field_unavailable_dates | Unavailable Dates | multiple_dates | 1 | false | config/sync/field.field.commerce_product.cab.field_unavailable_dates.yml |
| field_vehicle_type | Vehicle Type | string | 1 | false | config/sync/field.field.commerce_product.cab.field_vehicle_type.yml |


## commerce_product.default (Default)
- Source: `config/sync/commerce_product.commerce_product_type.default.yml`
- Business purpose: Commerce product bundle for travel catalog/booking inventory.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Body | text_with_summary | 1 | false | config/sync/field.field.commerce_product.default.body.yml |


## commerce_product.package (Package)
- Source: `config/sync/commerce_product.commerce_product_type.package.yml`
- Business purpose: Commerce product bundle for travel catalog/booking inventory.
- Relationships: `field_destination`, `field_featured_image`, `field_location_type`, `field_package_type`, `field_pdf`, `field_region`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Overview | text_with_summary | 1 | false | config/sync/field.field.commerce_product.package.body.yml |
| field_comparison_text | Comparison Text | text_long | 1 | false | config/sync/field.field.commerce_product.package.field_comparison_text.yml |
| field_deposit_percentage | Deposit Percentage | integer | 1 | false | config/sync/field.field.commerce_product.package.field_deposit_percentage.yml |
| field_destination | Destination | entity_reference | 1 | false | config/sync/field.field.commerce_product.package.field_destination.yml |
| field_disable_booking | Disable Booking | boolean | 1 | false | config/sync/field.field.commerce_product.package.field_disable_booking.yml |
| field_duration | Duration | string | 1 | false | config/sync/field.field.commerce_product.package.field_duration.yml |
| field_featured | Featured | boolean | 1 | false | config/sync/field.field.commerce_product.package.field_featured.yml |
| field_featured_image | Featured Image | entity_reference | 1 | false | config/sync/field.field.commerce_product.package.field_featured_image.yml |
| field_featured_variation | Featured Variation | link | 1 | false | config/sync/field.field.commerce_product.package.field_featured_variation.yml |
| field_gallery_label | Gallery Label | string | 1 | false | config/sync/field.field.commerce_product.package.field_gallery_label.yml |
| field_location_type | Location Type | entity_reference | 1 | false | config/sync/field.field.commerce_product.package.field_location_type.yml |
| field_message_to_customer | Message to Customer | string_long | 1 | false | config/sync/field.field.commerce_product.package.field_message_to_customer.yml |
| field_meta_tags | Meta Tags | metatag | 1 | false | config/sync/field.field.commerce_product.package.field_meta_tags.yml |
| field_other_infos | Package Infos | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.package.field_other_infos.yml |
| field_package_type | Package Type | entity_reference | 1 | false | config/sync/field.field.commerce_product.package.field_package_type.yml |
| field_pdf | Attachment | file | 1 | false | config/sync/field.field.commerce_product.package.field_pdf.yml |
| field_product_type_comment | Variation Message | string_long | 1 | false | config/sync/field.field.commerce_product.package.field_product_type_comment.yml |
| field_rating | Rating | fivestar | 1 | false | config/sync/field.field.commerce_product.package.field_rating.yml |
| field_region | Region | entity_reference | 1 | false | config/sync/field.field.commerce_product.package.field_region.yml |
| field_sold_out | Sold Out | boolean | 1 | false | config/sync/field.field.commerce_product.package.field_sold_out.yml |
| field_special_badge | Special Badge | string | 1 | false | config/sync/field.field.commerce_product.package.field_special_badge.yml |
| field_unavailable_dates | Unavailable Dates | multiple_dates | 1 | false | config/sync/field.field.commerce_product.package.field_unavailable_dates.yml |


## commerce_product.room (Stay)
- Source: `config/sync/commerce_product.commerce_product_type.room.yml`
- Business purpose: Commerce product bundle for travel catalog/booking inventory.
- Relationships: `field_addon`, `field_destination`, `field_featured_image`, `field_media`, `field_related_room`, `field_related_variation`, `field_room_type`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Overview | text_with_summary | 1 | false | config/sync/field.field.commerce_product.room.body.yml |
| field_addon | Addon | entity_reference | 1 | false | config/sync/field.field.commerce_product.room.field_addon.yml |
| field_amneties | Amneties | text_long | 1 | false | config/sync/field.field.commerce_product.room.field_amneties.yml |
| field_availability | Availability | integer | 1 | false | config/sync/field.field.commerce_product.room.field_availability.yml |
| field_deposit_percentage | Deposit Percentage | integer | 1 | false | config/sync/field.field.commerce_product.room.field_deposit_percentage.yml |
| field_destination | Destination | entity_reference | 1 | false | config/sync/field.field.commerce_product.room.field_destination.yml |
| field_disable_booking | Disable Booking | boolean | 1 | false | config/sync/field.field.commerce_product.room.field_disable_booking.yml |
| field_featured | Featured | boolean | 1 | false | config/sync/field.field.commerce_product.room.field_featured.yml |
| field_featured_image | Featured Image | entity_reference | 1 | false | config/sync/field.field.commerce_product.room.field_featured_image.yml |
| field_gallery_label | Gallery Label | string | 1 | false | config/sync/field.field.commerce_product.room.field_gallery_label.yml |
| field_key_points | Key Points | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.room.field_key_points.yml |
| field_location | Location | string | 1 | false | config/sync/field.field.commerce_product.room.field_location.yml |
| field_map_embed | Map Embed | string_long | 1 | false | config/sync/field.field.commerce_product.room.field_map_embed.yml |
| field_media | Media | entity_reference | -1 | false | config/sync/field.field.commerce_product.room.field_media.yml |
| field_meta_tags | Meta Tags | metatag | 1 | false | config/sync/field.field.commerce_product.room.field_meta_tags.yml |
| field_product_type_comment | Variation Message | string_long | 1 | false | config/sync/field.field.commerce_product.room.field_product_type_comment.yml |
| field_related_room | Related Room | entity_reference | 4 | false | config/sync/field.field.commerce_product.room.field_related_room.yml |
| field_related_variation | Related Variation | entity_reference | -1 | false | config/sync/field.field.commerce_product.room.field_related_variation.yml |
| field_room_type | Type | entity_reference | 1 | false | config/sync/field.field.commerce_product.room.field_room_type.yml |
| field_sold_out | Sold Out | boolean | 1 | false | config/sync/field.field.commerce_product.room.field_sold_out.yml |
| field_unavailable_dates | Unavailable Dates | multiple_dates | 1 | false | config/sync/field.field.commerce_product.room.field_unavailable_dates.yml |


## commerce_product.trip (Event)
- Source: `config/sync/commerce_product.commerce_product_type.trip.yml`
- Business purpose: Commerce product bundle for travel catalog/booking inventory.
- Relationships: `field_destination`, `field_featured_image`, `field_location_type`, `field_media`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Overview | text_with_summary | 1 | false | config/sync/field.field.commerce_product.trip.body.yml |
| field_blocks | Blocks | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.trip.field_blocks.yml |
| field_date | Start Date | datetime | 1 | false | config/sync/field.field.commerce_product.trip.field_date.yml |
| field_deposit_percentage | Deposit Percentage | integer | 1 | false | config/sync/field.field.commerce_product.trip.field_deposit_percentage.yml |
| field_destination | Destination | entity_reference | 1 | false | config/sync/field.field.commerce_product.trip.field_destination.yml |
| field_disable_booking | Disable Booking | boolean | 1 | false | config/sync/field.field.commerce_product.trip.field_disable_booking.yml |
| field_duration | Duration | string | 1 | false | config/sync/field.field.commerce_product.trip.field_duration.yml |
| field_end_date | End Date | datetime | 1 | false | config/sync/field.field.commerce_product.trip.field_end_date.yml |
| field_exclusion | Exclusions | text_long | 1 | false | config/sync/field.field.commerce_product.trip.field_exclusion.yml |
| field_featured_image | Featured Image | entity_reference | 1 | false | config/sync/field.field.commerce_product.trip.field_featured_image.yml |
| field_gallery_label | Gallery Label | string | 1 | false | config/sync/field.field.commerce_product.trip.field_gallery_label.yml |
| field_inclusion | Inclusions | text_long | 1 | false | config/sync/field.field.commerce_product.trip.field_inclusion.yml |
| field_itenary | Tour Plan | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.trip.field_itenary.yml |
| field_key_points | Key Points | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.trip.field_key_points.yml |
| field_location_type | Location Type | entity_reference | 1 | false | config/sync/field.field.commerce_product.trip.field_location_type.yml |
| field_media | Media | entity_reference | -1 | false | config/sync/field.field.commerce_product.trip.field_media.yml |
| field_meta_tags | Meta Tags | metatag | 1 | false | config/sync/field.field.commerce_product.trip.field_meta_tags.yml |
| field_other_infos | Event Infos | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.trip.field_other_infos.yml |
| field_sold_out | Sold Out | boolean | 1 | false | config/sync/field.field.commerce_product.trip.field_sold_out.yml |
| field_stock | Availability | commerce_stock_level | 1 | false | config/sync/field.field.commerce_product.trip.field_stock.yml |


## commerce_product.weekend_trip (Weekend Trip)
- Source: `config/sync/commerce_product.commerce_product_type.weekend_trip.yml`
- Business purpose: Commerce product bundle for travel catalog/booking inventory.
- Relationships: `field_destination`, `field_featured_image`, `field_media`, `field_organiser`, `field_pdf`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Overview | text_with_summary | 1 | false | config/sync/field.field.commerce_product.weekend_trip.body.yml |
| field_availability | Availability | integer | 1 | true | config/sync/field.field.commerce_product.weekend_trip.field_availability.yml |
| field_available_dates | Available Dates | multiple_dates | 1 | true | config/sync/field.field.commerce_product.weekend_trip.field_available_dates.yml |
| field_deposit_percentage | Deposit Percentage | integer | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_deposit_percentage.yml |
| field_destination | Destination | entity_reference | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_destination.yml |
| field_disable_booking | Disable Booking | boolean | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_disable_booking.yml |
| field_duration | Duration | string | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_duration.yml |
| field_featured_image | Featured Image | entity_reference | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_featured_image.yml |
| field_gallery_label | Gallery Label | string | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_gallery_label.yml |
| field_group_size | Group of | string | 1 | true | config/sync/field.field.commerce_product.weekend_trip.field_group_size.yml |
| field_itenary | Tour Plan | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.weekend_trip.field_itenary.yml |
| field_key_points | Key Points | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.weekend_trip.field_key_points.yml |
| field_media | Media | entity_reference | -1 | false | config/sync/field.field.commerce_product.weekend_trip.field_media.yml |
| field_meta_tags | Meta Tags | metatag | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_meta_tags.yml |
| field_organiser | Organiser | entity_reference | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_organiser.yml |
| field_other_infos | Trip Infos | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product.weekend_trip.field_other_infos.yml |
| field_pdf | Attachment | file | 1 | false | config/sync/field.field.commerce_product.weekend_trip.field_pdf.yml |


## commerce_product_variation.cab (Cab)
- Source: `config/sync/commerce_product.commerce_product_variation_type.cab.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `attribute_pickup_drop`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| attribute_pickup_drop | Pickup & Drop | entity_reference | 1 | true | config/sync/field.field.commerce_product_variation.cab.attribute_pickup_drop.yml |


## commerce_product_variation.default (Default)
- Source: `config/sync/commerce_product.commerce_product_variation_type.default.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## commerce_product_variation.package (Package)
- Source: `config/sync/commerce_product.commerce_product_variation_type.package.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `attribute_package_type`, `field_media`, `field_video_gallery`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| attribute_package_type | Package Type | entity_reference | 1 | true | config/sync/field.field.commerce_product_variation.package.attribute_package_type.yml |
| field_disable_booking | Disable Booking | boolean | 1 | false | config/sync/field.field.commerce_product_variation.package.field_disable_booking.yml |
| field_exclusion | Exclusions | text_long | 1 | false | config/sync/field.field.commerce_product_variation.package.field_exclusion.yml |
| field_inclusion | Inclusions | text_long | 1 | false | config/sync/field.field.commerce_product_variation.package.field_inclusion.yml |
| field_itenary | Tour Plan | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product_variation.package.field_itenary.yml |
| field_key_points | Key Points | entity_reference_revisions | -1 | false | config/sync/field.field.commerce_product_variation.package.field_key_points.yml |
| field_media | Media | entity_reference | -1 | false | config/sync/field.field.commerce_product_variation.package.field_media.yml |
| field_unavailable_dates | Unavailable Dates | multiple_dates | 1 | false | config/sync/field.field.commerce_product_variation.package.field_unavailable_dates.yml |
| field_video_gallery | Video Gallery | entity_reference | -1 | false | config/sync/field.field.commerce_product_variation.package.field_video_gallery.yml |
| maximum_order_quantity | Maximum quantity per order | integer | 1 | false | config/sync/field.field.commerce_product_variation.package.maximum_order_quantity.yml |
| minimum_order_quantity | Minimum quantity per order | integer | 1 | false | config/sync/field.field.commerce_product_variation.package.minimum_order_quantity.yml |


## commerce_product_variation.room (Stay)
- Source: `config/sync/commerce_product.commerce_product_variation_type.room.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## commerce_product_variation.trip (Event)
- Source: `config/sync/commerce_product.commerce_product_variation_type.trip.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## commerce_product_variation.weekend_trip (Weekend Trip)
- Source: `config/sync/commerce_product.commerce_product_variation_type.weekend_trip.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## media.audio (Audio)
- Source: `config/sync/media.type.audio.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_media_audio_file`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_media_audio_file | Audio file | file | 1 | true | config/sync/field.field.media.audio.field_media_audio_file.yml |


## media.document (Document)
- Source: `config/sync/media.type.document.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_media_document`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_media_document | Document | file | 1 | true | config/sync/field.field.media.document.field_media_document.yml |


## media.image (Image)
- Source: `config/sync/media.type.image.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_media_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_media_image | Image | image | 1 | true | config/sync/field.field.media.image.field_media_image.yml |


## media.remote_video (Remote video)
- Source: `config/sync/media.type.remote_video.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_media_oembed_video | Video URL | string | 1 | true | config/sync/field.field.media.remote_video.field_media_oembed_video.yml |


## media.video (Video)
- Source: `config/sync/media.type.video.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_media_video_file`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_media_video_file | Video file | file | 1 | true | config/sync/field.field.media.video.field_media_video_file.yml |


## node.article (Blog)
- Source: `config/sync/node.type.article.yml`
- Business purpose: Editorial/content bundle.
- Relationships: `field_image`, `field_tags`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Body | text_with_summary | 1 | false | config/sync/field.field.node.article.body.yml |
| field_image | Image | image | 1 | false | config/sync/field.field.node.article.field_image.yml |
| field_metatags | Metatags | metatag | 1 | false | config/sync/field.field.node.article.field_metatags.yml |
| field_tags | Tags | entity_reference | -1 | false | config/sync/field.field.node.article.field_tags.yml |


## node.destination (Destination)
- Source: `config/sync/node.type.destination.yml`
- Business purpose: Editorial/content bundle.
- Relationships: `field_icon`, `field_image`, `field_region`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Overview | text_with_summary | 1 | false | config/sync/field.field.node.destination.body.yml |
| field_attractions | Places of Interest | entity_reference_revisions | -1 | false | config/sync/field.field.node.destination.field_attractions.yml |
| field_featured | Featured | list_string | -1 | false | config/sync/field.field.node.destination.field_featured.yml |
| field_icon | Icon | image | 1 | false | config/sync/field.field.node.destination.field_icon.yml |
| field_image | Image | image | 1 | false | config/sync/field.field.node.destination.field_image.yml |
| field_metatags | Metatags | metatag | 1 | false | config/sync/field.field.node.destination.field_metatags.yml |
| field_region | Region | entity_reference | 1 | false | config/sync/field.field.node.destination.field_region.yml |


## node.flexslider_example (FlexSlider Example)
- Source: `config/sync/node.type.flexslider_example.yml`
- Business purpose: Editorial/content bundle.
- Relationships: `field_flexslider_example_image`, `field_flexslider_example_slidesh`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_flexslider_example_image | FlexSlider Example Image | image | -1 | false | config/sync/field.field.node.flexslider_example.field_flexslider_example_image.yml |
| field_flexslider_example_slidesh | FlexSlider Example Slideshow | image | -1 | false | config/sync/field.field.node.flexslider_example.field_flexslider_example_slidesh.yml |


## node.page (Page)
- Source: `config/sync/node.type.page.yml`
- Business purpose: Editorial/content bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Body | text_with_summary | 1 | false | config/sync/field.field.node.page.body.yml |
| field_image | Image | image | 1 | false | config/sync/field.field.node.page.field_image.yml |


## node.team (Team)
- Source: `config/sync/node.type.team.yml`
- Business purpose: Editorial/content bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Bio | text_with_summary | 1 | false | config/sync/field.field.node.team.body.yml |
| field_designation | Designation | string | 1 | true | config/sync/field.field.node.team.field_designation.yml |
| field_email | Email | email | 1 | false | config/sync/field.field.node.team.field_email.yml |
| field_facebook | Facebook | link | 1 | false | config/sync/field.field.node.team.field_facebook.yml |
| field_image | Image | image | 1 | false | config/sync/field.field.node.team.field_image.yml |
| field_instagram | Instagram | link | 1 | false | config/sync/field.field.node.team.field_instagram.yml |
| field_linkedin | LinkedIn | link | 1 | false | config/sync/field.field.node.team.field_linkedin.yml |
| field_x | X | link | 1 | false | config/sync/field.field.node.team.field_x.yml |


## node.testimonial (Testimonial)
- Source: `config/sync/node.type.testimonial.yml`
- Business purpose: Editorial/content bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| body | Testimony | text_with_summary | 1 | false | config/sync/field.field.node.testimonial.body.yml |
| field_image | DP | image | 1 | false | config/sync/field.field.node.testimonial.field_image.yml |
| field_location | Location | string | 1 | false | config/sync/field.field.node.testimonial.field_location.yml |
| field_star_rating | Star Rating | fivestar | 1 | false | config/sync/field.field.node.testimonial.field_star_rating.yml |


## paragraph.accordion (Accordion)
- Source: `config/sync/paragraphs.paragraphs_type.accordion.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_text | Text | text_long | 1 | false | config/sync/field.field.paragraph.accordion.field_text.yml |
| field_title | Title | string | 1 | false | config/sync/field.field.paragraph.accordion.field_title.yml |


## paragraph.cab_points (Cab Points)
- Source: `config/sync/paragraphs.paragraphs_type.cab_points.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_cab_key | Key | list_string | 1 | false | config/sync/field.field.paragraph.cab_points.field_cab_key.yml |
| field_value | Value | string | 1 | false | config/sync/field.field.paragraph.cab_points.field_value.yml |


## paragraph.image_and_text (Image and Text)
- Source: `config/sync/paragraphs.paragraphs_type.image_and_text.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_image | Image | image | -1 | false | config/sync/field.field.paragraph.image_and_text.field_image.yml |
| field_text | Text | text_long | 1 | false | config/sync/field.field.paragraph.image_and_text.field_text.yml |


## paragraph.image_gallery (Image Gallery)
- Source: `config/sync/paragraphs.paragraphs_type.image_gallery.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_media_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_media_image | Image | entity_reference | -1 | false | config/sync/field.field.paragraph.image_gallery.field_media_image.yml |


## paragraph.itenary (Itenary)
- Source: `config/sync/paragraphs.paragraphs_type.itenary.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_text | Text | text_long | 1 | false | config/sync/field.field.paragraph.itenary.field_text.yml |
| field_title | Title | string | 1 | false | config/sync/field.field.paragraph.itenary.field_title.yml |


## paragraph.left_image_with_text (Left Image with Text)
- Source: `config/sync/paragraphs.paragraphs_type.left_image_with_text.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_image | Image | image | -1 | false | config/sync/field.field.paragraph.left_image_with_text.field_image.yml |
| field_text | Text | text_long | 1 | false | config/sync/field.field.paragraph.left_image_with_text.field_text.yml |


## paragraph.package_points (Package Points)
- Source: `config/sync/paragraphs.paragraphs_type.package_points.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_key`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_key | Key | entity_reference | 1 | false | config/sync/field.field.paragraph.package_points.field_key.yml |
| field_value | Value | string | 1 | false | config/sync/field.field.paragraph.package_points.field_value.yml |


## paragraph.right_image_with_text (Right Image with text)
- Source: `config/sync/paragraphs.paragraphs_type.right_image_with_text.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_image | Image | image | -1 | false | config/sync/field.field.paragraph.right_image_with_text.field_image.yml |
| field_text | Text | text_long | 1 | false | config/sync/field.field.paragraph.right_image_with_text.field_text.yml |


## paragraph.text_only (Text Only)
- Source: `config/sync/paragraphs.paragraphs_type.text_only.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_text | Text | text_long | 1 | false | config/sync/field.field.paragraph.text_only.field_text.yml |
| field_title | Title | string | 1 | false | config/sync/field.field.paragraph.text_only.field_title.yml |


## paragraph.title_only (Title Only)
- Source: `config/sync/paragraphs.paragraphs_type.title_only.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_title | Title | string | 1 | false | config/sync/field.field.paragraph.title_only.field_title.yml |


## profile.customer (Customer)
- Source: `config/sync/profile.type.customer.yml`
- Business purpose: Drupal configuration entity bundle.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| address | Address | address | 1 | true | config/sync/field.field.profile.customer.address.yml |
| field_alternate_mobile_no | Alternate Mobile No. | phone_number | 1 | false | config/sync/field.field.profile.customer.field_alternate_mobile_no.yml |
| field_mobile_no | Mobile No. | phone_number | 1 | false | config/sync/field.field.profile.customer.field_mobile_no.yml |


## taxonomy_term.location_type (Location Type)
- Source: `config/sync/taxonomy.vocabulary.location_type.yml`
- Business purpose: Classification vocabulary.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## taxonomy_term.package_key (Package Key)
- Source: `config/sync/taxonomy.vocabulary.package_key.yml`
- Business purpose: Classification vocabulary.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_image | Image | image | 1 | true | config/sync/field.field.taxonomy_term.package_key.field_image.yml |


## taxonomy_term.package_type (Package Type)
- Source: `config/sync/taxonomy.vocabulary.package_type.yml`
- Business purpose: Classification vocabulary.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## taxonomy_term.partners (Partners)
- Source: `config/sync/taxonomy.vocabulary.partners.yml`
- Business purpose: Classification vocabulary.
- Relationships: `field_logo`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_logo | Logo | image | 1 | false | config/sync/field.field.taxonomy_term.partners.field_logo.yml |


## taxonomy_term.regions (Regions)
- Source: `config/sync/taxonomy.vocabulary.regions.yml`
- Business purpose: Classification vocabulary.
- Relationships: `field_image`
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
| field_deposit_percentage | Deposit Percentage | integer | 1 | false | config/sync/field.field.taxonomy_term.regions.field_deposit_percentage.yml |
| field_image | Image | image | 1 | true | config/sync/field.field.taxonomy_term.regions.field_image.yml |
| field_metatags | Metatags | metatag | 1 | false | config/sync/field.field.taxonomy_term.regions.field_metatags.yml |


## taxonomy_term.room_type (Room Type)
- Source: `config/sync/taxonomy.vocabulary.room_type.yml`
- Business purpose: Classification vocabulary.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |


## taxonomy_term.tags (Tags)
- Source: `config/sync/taxonomy.vocabulary.tags.yml`
- Business purpose: Classification vocabulary.
- Relationships: None detected from field types
- Validation: Confirmed field required/cardinality metadata where present in field.field and field.storage config.

| Field | Label | Type | Cardinality | Required | Config |
| --- | --- | --- | --- | --- | --- |
