## Batch Delete Catalog Objects Response

### Structure

`BatchDeleteCatalogObjectsResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | The set of [Error](./models/error.md)s encountered. |
| `deleted_object_ids` | `Array<String>` | Optional | The IDs of all [CatalogObject](./models/catalog-object.md)s deleted by this request. |
| `deleted_at` | `String` | Optional | The database [timestamp](#workingwithdates) of this deletion in RFC 3339 format, e.g., "2016-09-04T23:59:33.123Z". |

### Example (as JSON)

```json
{
  "deleted_object_ids": [
    "W62UWFY35CWMYGVWK6TWJDNI",
    "AA27W3M2GGTF3H6AVPNB77CK"
  ],
  "deleted_at": "2016-11-16T22:25:24.878Z"
}
```

