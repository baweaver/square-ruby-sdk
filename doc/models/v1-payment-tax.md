## V1 Payment Tax

V1PaymentTax

### Structure

`V1PaymentTax`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | Any errors that occurred during the request. |
| `name` | `String` | Optional | The merchant-defined name of the tax. |
| `applied_money` | [`V1 Money Hash`](/doc/models/v1-money.md) | Optional | - |
| `rate` | `String` | Optional | The rate of the tax, as a string representation of a decimal number. A value of 0.07 corresponds to a rate of 7%. |
| `inclusion_type` | [`String (V1 Fee Inclusion Type)`](/doc/models/v1-fee-inclusion-type.md) | Optional | - |
| `fee_id` | `String` | Optional | The ID of the tax, if available. Taxes applied in older versions of Square Register might not have an ID. |

### Example (as JSON)

```json
{
  "errors": null,
  "name": null,
  "applied_money": null,
  "rate": null,
  "inclusion_type": null,
  "fee_id": null
}
```

