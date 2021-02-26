
# Loyalty Account

Describes a loyalty account. For more information, see
[Loyalty Overview](https://developer.squareup.com/docs/loyalty/overview).

## Structure

`Loyalty Account`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | The Square-assigned ID of the loyalty account.<br>**Constraints**: *Maximum Length*: `36` |
| `mappings` | [`Array<Loyalty Account Mapping Hash>`](/doc/models/loyalty-account-mapping.md) | Required | The list of mappings that the account is associated with.<br>Currently, a buyer can only be mapped to a loyalty account using<br>a phone number. Therefore, the list can only have one mapping. |
| `program_id` | `String` | Required | The Square-assigned ID of the [loyalty program](#type-LoyaltyProgram) to which the account belongs.<br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `balance` | `Integer` | Optional | The available point balance in the loyalty account.<br><br>Your application should be able to handle loyalty accounts that have a negative point balance (`balance` is less than 0). This might occur if a seller makes a manual adjustment or as a result of a refund or exchange. |
| `lifetime_points` | `Integer` | Optional | The total points accrued during the lifetime of the account. |
| `customer_id` | `String` | Optional | The Square-assigned ID of the [customer](#type-Customer) that is associated with the account. |
| `enrolled_at` | `String` | Optional | The timestamp when enrollment occurred, in RFC 3339 format. |
| `created_at` | `String` | Optional | The timestamp when the loyalty account was created, in RFC 3339 format. |
| `updated_at` | `String` | Optional | The timestamp when the loyalty account was last updated, in RFC 3339 format. |

## Example (as JSON)

```json
{
  "id": "id0",
  "mappings": [
    {
      "id": "id4",
      "type": "type6",
      "value": "value6",
      "created_at": "created_at8"
    }
  ],
  "program_id": "program_id0",
  "balance": 64,
  "lifetime_points": 88,
  "customer_id": "customer_id8",
  "enrolled_at": "enrolled_at0"
}
```

