## Batch Retrieve Inventory Counts Response

### Structure

`BatchRetrieveInventoryCountsResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | Any errors that occurred during the request. |
| `counts` | [`Array<Inventory Count Hash>`](/doc/models/inventory-count.md) | Optional | The current calculated inventory counts for the requested objects<br>and locations. |
| `cursor` | `String` | Optional | The pagination cursor to be used in a subsequent request. If unset,<br>this is the final response.<br><br>See [Pagination](https://developer.squareup.com/docs/basics/api101/pagination) for more information. |

### Example (as JSON)

```json
{
  "errors": [],
  "counts": [
    {
      "catalog_object_id": "W62UWFY35CWMYGVWK6TWJDNI",
      "catalog_object_type": "ITEM_VARIATION",
      "state": "IN_STOCK",
      "location_id": "59TNP9SA8VGDA",
      "quantity": "79",
      "calculated_at": "2016-11-16T22:28:01.223Z"
    }
  ]
}
```

