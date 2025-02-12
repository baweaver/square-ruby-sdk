## Catalog Item Option Value for Item Variation

A [CatalogItemOptionValue](./models/catalog-item-option-value.md) links an item
variation to an item option as an item option value. For example, a t-shirt
item may offer a color option and a size option. An item option value
would represent each variation of t-shirt: For example, “Color:Red, Size:Small”
or “Color:Blue, Size:Medium”.

### Structure

`CatalogItemOptionValueForItemVariation`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item_option_id` | `String` | Optional | The unique id of an item option. |
| `item_option_value_id` | `String` | Optional | The unique id of the selected value for the item option. |

### Example (as JSON)

```json
{
  "item_option_id": null,
  "item_option_value_id": null
}
```

