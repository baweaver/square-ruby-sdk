## Create Payment Request

Creates a payment from the source (nonce, card on file, etc.)

The `PAYMENTS_WRITE_ADDITIONAL_RECIPIENTS` OAuth permission is required
to enable application fees.

For more information, see [Payments and Refunds Overview](https://developer.squareup.com/docs/payments-api/overview).

For information about application fees in a payment, see
[Collect Fees](https://developer.squareup.com/docs/payments-api/take-payments-and-collect-fees).

### Structure

`CreatePaymentRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `source_id` | `String` |  | The ID for the source of funds for this payment.  This can be a nonce<br>generated by the Payment Form or a card on file made with the Customers API. |
| `idempotency_key` | `String` |  | A unique string that identifies this CreatePayment request. Keys can be any valid string but<br>must be unique for every CreatePayment request.<br><br>Max: 45 characters<br><br>See [Idempotency keys](https://developer.squareup.com/docs/basics/api101/idempotency) for more information. |
| `amount_money` | [`Money Hash`](/doc/models/money.md) |  | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `tip_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `app_fee_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `autocomplete` | `Boolean` | Optional | If set to `true`, this payment will be completed when possible. If<br>set to `false`, this payment will be held in an approved state until either<br>explicitly completed or canceled. For more information, see<br>[Delayed Payments](https://developer.squareup.com/docs/payments-api/take-payments#delayed-payments).<br><br>Default: true |
| `order_id` | `String` | Optional | Associate a previously created order with this payment |
| `customer_id` | `String` | Optional | The ID of the customer associated with the payment.<br>Required if the `source_id` refers to a card on file created using the<br>Customers API. |
| `location_id` | `String` | Optional | The location ID to associate with the payment. If not specified, the default location is used. |
| `reference_id` | `String` | Optional | A user-defined ID to associate with the payment.<br>You can use this field to associate the payment to an entity in an external system.<br>For example, you might specify an order ID that is generated by a third-party shopping cart.<br><br>Limit 40 characters. |
| `verification_token` | `String` | Optional | An identifying token generated by `SqPaymentForm.verifyBuyer()`.<br>Verification tokens encapsulate customer device information and 3-D Secure<br>challenge results to indicate that Square has verified the buyer identity.<br><br>See the [SCA Overview](https://developer.squareup.com/docs/sca-overview) for more. |
| `accept_partial_authorization` | `Boolean` | Optional | If set to true and charging a Square Gift Card, a payment may be returned with<br>amount_money equal to less than what was requested.  Example, a request for $20 when charging<br>a Square Gift Card with balance of $5 wil result in an APPROVED payment of $5.  You may choose<br>to prompt the buyer for an additional payment to cover the remainder, or cancel the gift card<br>payment.  Cannot be `true` when `autocomplete = true<br><br>For more information, see<br>[Partial amount with Square gift cards](https://developer.squareup.com/docs/payments-api/take-payments#partial-payment-gift-card).<br><br>Default: false |
| `buyer_email_address` | `String` | Optional | The buyer's e-mail address |
| `billing_address` | [`Address Hash`](/doc/models/address.md) | Optional | Represents a physical address. |
| `shipping_address` | [`Address Hash`](/doc/models/address.md) | Optional | Represents a physical address. |
| `note` | `String` | Optional | An optional note to be entered by the developer when creating a payment<br><br>Limit 500 characters. |

### Example (as JSON)

```json
{
  "idempotency_key": "4935a656-a929-4792-b97c-8848be85c27c",
  "amount_money": {
    "amount": 200,
    "currency": "USD"
  },
  "source_id": "ccof:uIbfJXhXETSP197M3GB",
  "autocomplete": true,
  "customer_id": "VDKXEEKPJN48QDG3BGGFAK05P8",
  "location_id": "XK3DBG77NJBFX",
  "reference_id": "123456",
  "note": "Brief description",
  "app_fee_money": {
    "amount": 10,
    "currency": "USD"
  }
}
```

