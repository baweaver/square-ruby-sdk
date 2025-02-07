## Catalog Id Mapping

A mapping between a client-supplied temporary ID and a permanent server ID.

### Structure

`CatalogIdMapping`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `client_object_id` | `String` | Optional | The client-supplied, temporary `#`-prefixed ID for a new [CatalogObject](./models/catalog-object.md). |
| `object_id` | `String` | Optional | The permanent ID for the [CatalogObject](./models/catalog-object.md) created by the server. |

### Example (as JSON)

```json
{
  "client_object_id": null,
  "object_id": null
}
```

