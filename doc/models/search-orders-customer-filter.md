
# Search Orders Customer Filter

Filter based on Order `customer_id` and any Tender `customer_id`
associated with the Order. Does not filter based on the
[FulfillmentRecipient](/doc/models/order-fulfillment-recipient.md) `customer_id`.

## Structure

`Search Orders Customer Filter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `customer_ids` | `Array<String>` | Optional | List of customer IDs to filter by.<br><br>Max: 10 customer IDs. |

## Example (as JSON)

```json
{
  "customer_ids": [
    "customer_ids1",
    "customer_ids2"
  ]
}
```

