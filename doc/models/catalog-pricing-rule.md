## Catalog Pricing Rule

Defines how prices are modified or set for items that match the pricing rule
during the active time period.

### Structure

`CatalogPricingRule`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | User-defined name for the pricing rule. For example, "Buy one get one<br>free" or "10% off". |
| `time_period_ids` | `Array<String>` | Optional | Unique ID for the [CatalogTimePeriod](./models/catalog-time-period.md)s when<br>this pricing rule is in effect. If left unset, the pricing rule is always<br>in effect. |
| `discount_id` | `String` | Optional | Unique ID for the [CatalogDiscount](./models/catalog-discount.md) to take off<br>the price of all matched items.<br><br>Only one of `total_price_money`, `item_price`, or `discount` can be supplied. |
| `match_products_id` | `String` | Optional | Unique ID for the [CatalogProductSet](./models/catalog-product-set.md) that will<br>be matched by this rule. A match rule matches within the entire cart. |
| `apply_products_id` | `String` | Optional | The [CatalogProductSet](./models/catalog-product-set.md) to apply the pricing rule to<br>within the set of matched products specified by `match_products_id`.<br>An apply rule can only match once within the set of matched products.<br>If left unset, the pricing rule will be applied to all products within the<br>set of matched products. |
| `exclude_products_id` | `String` | Optional | Identifies the [CatalogProductSet](./models/catalog-product-set.md) to exclude<br>from this pricing rule.<br>An exclude rule matches within the subset of the cart that fits the match rules (the match set).<br>An exclude rule can only match once in the match set.<br>If not supplied, the pricing will be applied to all products in the match set.<br>Other products retain their base price, or a price generated by other rules. |
| `valid_from_date` | `String` | Optional | Represents the date the Pricing Rule is valid from. Represented in<br>RFC3339 full-date format (YYYY-MM-DD). |
| `valid_from_local_time` | `String` | Optional | Represents the local time the pricing rule should be valid from. Time<br>zone is determined by the device running the Point of Sale app.<br><br>Represented in RFC3339 partial-time format (HH:MM:SS). Partial seconds will be truncated. |
| `valid_until_date` | `String` | Optional | Represents the date the pricing rule will become inactive.<br><br>Represented in RFC3339 full-date format (YYYY-MM-DD). |
| `valid_until_local_time` | `String` | Optional | Represents the local time at which the pricing rule will become inactive.<br>Time zone is determined by the device running the Point of Sale app.<br><br>Represented in RFC3339 partial-time format<br>(HH:MM:SS). Partial seconds will be truncated. |

### Example (as JSON)

```json
{
  "name": null,
  "time_period_ids": null,
  "discount_id": null,
  "match_products_id": null,
  "apply_products_id": null,
  "exclude_products_id": null,
  "valid_from_date": null,
  "valid_from_local_time": null,
  "valid_until_date": null,
  "valid_until_local_time": null
}
```

