## V1 Create Refund Request

V1CreateRefundRequest

### Structure

`V1CreateRefundRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payment_id` | `String` |  | The ID of the payment to refund. If you are creating a `PARTIAL`<br>refund for a split tender payment, instead provide the id of the<br>particular tender you want to refund. |
| `type` | [`String (V1 Create Refund Request Type)`](/doc/models/v1-create-refund-request-type.md) |  | - |
| `reason` | `String` |  | The reason for the refund. |
| `refunded_money` | [`V1 Money Hash`](/doc/models/v1-money.md) | Optional | - |
| `request_idempotence_key` | `String` | Optional | An optional key to ensure idempotence if you issue the same PARTIAL refund request more than once. |

### Example (as JSON)

```json
{
  "payment_id": "payment_id0",
  "type": "FULL",
  "reason": "reason4",
  "refunded_money": null,
  "request_idempotence_key": null
}
```

