## List Catalog Response

### Structure

`ListCatalogResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | The set of [Error](./models/error.md)s encountered. |
| `cursor` | `String` | Optional | The pagination cursor to be used in a subsequent request. If unset, this is the final response.<br>See [Pagination](https://developer.squareup.com/docs/basics/api101/pagination) for more information. |
| `objects` | [`Array<Catalog Object Hash>`](/doc/models/catalog-object.md) | Optional | The [CatalogObject](./models/catalog-object.md)s returned. |

### Example (as JSON)

```json
{
  "objects": [
    {
      "type": "CATEGORY",
      "id": "5ZYQZZ2IECPVJ2IJ5KQPRDC3",
      "updated_at": "2017-02-21T14:50:26.495Z",
      "version": 1487688626495,
      "is_deleted": false,
      "present_at_all_locations": true,
      "category_data": {
        "name": "Beverages"
      }
    },
    {
      "type": "TAX",
      "id": "L5R47DGBZOOVKCAFIXC56AEN",
      "updated_at": "2017-02-21T14:50:26.495Z",
      "version": 1487688626495,
      "is_deleted": false,
      "present_at_all_locations": true,
      "tax_data": {
        "name": "Sales Tax",
        "calculation_phase": "TAX_SUBTOTAL_PHASE",
        "inclusion_type": "ADDITIVE",
        "percentage": "5.0",
        "enabled": true
      }
    }
  ]
}
```

