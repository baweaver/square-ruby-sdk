## Catalog Query Range

### Structure

`CatalogQueryRange`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attribute_name` | `String` |  | The name of the attribute to be searched. |
| `attribute_min_value` | `Long` | Optional | The desired minimum value for the search attribute (inclusive). |
| `attribute_max_value` | `Long` | Optional | The desired maximum value for the search attribute (inclusive). |

### Example (as JSON)

```json
{
  "attribute_name": "attribute_name4",
  "attribute_min_value": null,
  "attribute_max_value": null
}
```

