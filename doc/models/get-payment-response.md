## Get Payment Response

Defines the fields that are included in the response body of
a request to the [GetPayment](/doc/payments.md#getpayment) endpoint.

### Structure

`GetPaymentResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | Information on errors encountered during the request. |
| `payment` | [`Payment Hash`](/doc/models/payment.md) | Optional | Represents a payment processed by the Square API. |

### Example (as JSON)

```json
{
  "payment": {
    "id": "iqrBxAil6rmDtr7cak9g9WO8uaB",
    "created_at": "2019-07-10T13:23:49.154Z",
    "updated_at": "2019-07-10T13:23:49.446Z",
    "amount_money": {
      "amount": 200,
      "currency": "USD"
    },
    "app_fee_money": {
      "amount": 10,
      "currency": "USD"
    },
    "total_money": {
      "amount": 200,
      "currency": "USD"
    },
    "status": "COMPLETED",
    "source_type": "CARD",
    "card_details": {
      "status": "CAPTURED",
      "card": {
        "card_brand": "VISA",
        "last_4": "2796",
        "exp_month": 7,
        "exp_year": 2026,
        "fingerprint": "sq-1-TpmjbNBMFdibiIjpQI5LiRgNUBC7u1689i0TgHjnlyHEWYB7tnn-K4QbW4ttvtaqXw"
      },
      "entry_method": "ON_FILE",
      "cvv_status": "CVV_ACCEPTED",
      "avs_status": "AVS_ACCEPTED",
      "auth_result_code": "nsAyY2"
    },
    "location_id": "XK3DBG77NJBFX",
    "order_id": "qHkNOb03hMgEgoP3gyzFBDY3cg4F",
    "reference_id": "123456",
    "note": "Brief description",
    "customer_id": "VDKXEEKPJN48QDG3BGGFAK05P8",
    "processing_fee": [
      {
        "effective_at": "2019-07-10T15:23:49.000Z",
        "type": "INITIAL",
        "amount_money": {
          "amount": 36,
          "currency": "USD"
        }
      }
    ]
  }
}
```

