## V1 Discount

V1Discount

### Structure

`V1Discount`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | The discount's unique ID. |
| `name` | `String` | Optional | The discount's name. |
| `rate` | `String` | Optional | The rate of the discount, as a string representation of a decimal number. A value of 0.07 corresponds to a rate of 7%. This rate is 0 if discount_type is VARIABLE_PERCENTAGE. |
| `amount_money` | [`V1 Money Hash`](/doc/models/v1-money.md) | Optional | - |
| `discount_type` | [`String (V1 Discount Discount Type)`](/doc/models/v1-discount-discount-type.md) | Optional | - |
| `pin_required` | `Boolean` | Optional | Indicates whether a mobile staff member needs to enter their PIN to apply the discount to a payment. |
| `color` | [`String (V1 Discount Color)`](/doc/models/v1-discount-color.md) | Optional | - |
| `v2_id` | `String` | Optional | The ID of the CatalogObject in the Connect v2 API. Objects that are shared across multiple locations share the same v2 ID. |

### Example (as JSON)

```json
{
  "id": null,
  "name": null,
  "rate": null,
  "amount_money": null,
  "discount_type": null,
  "pin_required": null,
  "color": null,
  "v2_id": null
}
```

