## V1 Variation

V1Variation

### Structure

`V1Variation`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | The item variation's unique ID. |
| `name` | `String` | Optional | The item variation's name. |
| `item_id` | `String` | Optional | The ID of the variation's associated item. |
| `ordinal` | `Integer` | Optional | Indicates the variation's list position when displayed in Square Register and the merchant dashboard. If more than one variation for the same item has the same ordinal value, those variations are displayed in alphabetical order |
| `pricing_type` | [`String (V1 Variation Pricing Type)`](/doc/models/v1-variation-pricing-type.md) | Optional | - |
| `price_money` | [`V1 Money Hash`](/doc/models/v1-money.md) | Optional | - |
| `sku` | `String` | Optional | The item variation's SKU, if any. |
| `track_inventory` | `Boolean` | Optional | If true, inventory tracking is active for the variation. |
| `inventory_alert_type` | [`String (V1 Variation Inventory Alert Type)`](/doc/models/v1-variation-inventory-alert-type.md) | Optional | - |
| `inventory_alert_threshold` | `Integer` | Optional | If the inventory quantity for the variation is less than or equal to this value and inventory_alert_type is LOW_QUANTITY, the variation displays an alert in the merchant dashboard. |
| `user_data` | `String` | Optional | Arbitrary metadata associated with the variation. Cannot exceed 255 characters. |
| `v2_id` | `String` | Optional | The ID of the CatalogObject in the Connect v2 API. Objects that are shared across multiple locations share the same v2 ID. |

### Example (as JSON)

```json
{
  "id": null,
  "name": null,
  "item_id": null,
  "ordinal": null,
  "pricing_type": null,
  "price_money": null,
  "sku": null,
  "track_inventory": null,
  "inventory_alert_type": null,
  "inventory_alert_threshold": null,
  "user_data": null,
  "v2_id": null
}
```

