## Retrieve Inventory Changes Response

### Structure

`RetrieveInventoryChangesResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | Any errors that occurred during the request. |
| `changes` | [`Array<Inventory Change Hash>`](/doc/models/inventory-change.md) | Optional | The set of inventory changes for the requested object and locations. |
| `cursor` | `String` | Optional | The pagination cursor to be used in a subsequent request. If unset,<br>this is the final response.<br><br>See [Pagination](https://developer.squareup.com/docs/basics/api101/pagination) for more information. |

### Example (as JSON)

```json
{
  "errors": [],
  "changes": [
    {
      "type": "ADJUSTMENT",
      "adjustment": {
        "id": "OJKJIUANKLMLQANZADNPLKAD",
        "reference_id": "d8207693-168f-4b44-a2fd-a7ff533ddd26",
        "from_state": "IN_STOCK",
        "to_state": "SOLD",
        "location_id": "C6W5YS5QM06F5",
        "catalog_object_id": "W62UWFY35CWMYGVWK6TWJDNI",
        "catalog_object_type": "ITEM_VARIATION",
        "quantity": "3",
        "total_price_money": {
          "amount": 5000,
          "currency": "USD"
        },
        "occurred_at": "2016-11-16T22:25:24.878Z",
        "created_at": "2016-11-16T22:25:24.878Z",
        "source": {
          "product": "SQUARE_POS",
          "application_id": "416ff29c-86c4-4feb-b58c-9705f21f3ea0",
          "name": "Square Point of Sale 4.37"
        },
        "employee_id": "AV7YRCGI2H1J5NQ8E1XIZCNA",
        "transaction_id": "5APV6JYK1SNCZD11AND2RX1Z"
      }
    }
  ]
}
```

