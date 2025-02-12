## Charge Request

Defines the parameters that can be included in the body of
a request to the [Charge](#endpoint-charge) endpoint.

Deprecated - recommend using [CreatePayment](/doc/payments.md#createpayment)

### Structure

`ChargeRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `idempotency_key` | `String` |  | A value you specify that uniquely identifies this<br>transaction among transactions you've created.<br><br>If you're unsure whether a particular transaction succeeded,<br>you can reattempt it with the same idempotency key without<br>worrying about double-charging the buyer.<br><br>See [Idempotency](https://developer.squareup.com/docs/basics/api101/idempotency) for more information. |
| `amount_money` | [`Money Hash`](/doc/models/money.md) |  | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `card_nonce` | `String` | Optional | A nonce generated from the `SqPaymentForm` that represents the card<br>to charge.<br><br>The application that provides a nonce to this endpoint must be the<br>_same application_ that generated the nonce with the `SqPaymentForm`.<br>Otherwise, the nonce is invalid.<br><br>Do not provide a value for this field if you provide a value for<br>`customer_card_id`. |
| `customer_card_id` | `String` | Optional | The ID of the customer card on file to charge. Do<br>not provide a value for this field if you provide a value for `card_nonce`.<br><br>If you provide this value, you _must_ also provide a value for<br>`customer_id`. |
| `delay_capture` | `Boolean` | Optional | If `true`, the request will only perform an Auth on the provided<br>card. You can then later perform either a Capture (with the<br>[CaptureTransaction](#endpoint-capturetransaction) endpoint) or a Void<br>(with the [VoidTransaction](#endpoint-voidtransaction) endpoint).<br><br>Default value: `false` |
| `reference_id` | `String` | Optional | An optional ID you can associate with the transaction for your own<br>purposes (such as to associate the transaction with an entity ID in your<br>own database).<br><br>This value cannot exceed 40 characters. |
| `note` | `String` | Optional | An optional note to associate with the transaction.<br><br>This value cannot exceed 60 characters. |
| `customer_id` | `String` | Optional | The ID of the customer to associate this transaction with. This field<br>is required if you provide a value for `customer_card_id`, and optional<br>otherwise. |
| `billing_address` | [`Address Hash`](/doc/models/address.md) | Optional | Represents a physical address. |
| `shipping_address` | [`Address Hash`](/doc/models/address.md) | Optional | Represents a physical address. |
| `buyer_email_address` | `String` | Optional | The buyer's email address, if available. |
| `order_id` | `String` | Optional | The ID of the order to associate with this transaction.<br><br>If you provide this value, the `amount_money` value of your request must<br>__exactly match__ the value of the order's `total_money` field. |
| `additional_recipients` | [`Array<Additional Recipient Hash>`](/doc/models/additional-recipient.md) | Optional | The basic primitive of multi-party transaction. The value is optional.<br>The transaction facilitated by you can be split from here.<br><br>If you provide this value, the `amount_money` value in your additional_recipients<br>must not be more than 90% of the `amount_money` value in the charge request.<br>The `location_id` must be the valid location of the app owner merchant.<br><br>This field requires the `PAYMENTS_WRITE_ADDITIONAL_RECIPIENTS` OAuth permission.<br><br>This field is currently not supported in sandbox. |
| `verification_token` | `String` | Optional | An identifying token generated by `SqPaymentForm.verifyBuyer()`.<br>Verification tokens encapsulate customer device information and 3-D Secure<br>challenge results to indicate that Square has verified the buyer identity. |

### Example (as JSON)

```json
{
  "idempotency_key": "74ae1696-b1e3-4328-af6d-f1e04d947a13",
  "shipping_address": {
    "address_line_1": "123 Main St",
    "locality": "San Francisco",
    "administrative_district_level_1": "CA",
    "postal_code": "94114",
    "country": "US"
  },
  "billing_address": {
    "address_line_1": "500 Electric Ave",
    "address_line_2": "Suite 600",
    "administrative_district_level_1": "NY",
    "locality": "New York",
    "postal_code": "10003",
    "country": "US"
  },
  "amount_money": {
    "amount": 200,
    "currency": "USD"
  },
  "additional_recipients": [
    {
      "location_id": "057P5VYJ4A5X1",
      "description": "Application fees",
      "amount_money": {
        "amount": 20,
        "currency": "USD"
      }
    }
  ],
  "card_nonce": "card_nonce_from_square_123",
  "reference_id": "some optional reference id",
  "note": "some optional note",
  "delay_capture": false
}
```

