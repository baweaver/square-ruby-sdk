## List Refunds Request

Defines the query parameters that can be included in
a request to the [ListRefunds](#endpoint-listrefunds) endpoint.

Deprecated - recommend using [SearchOrders](/doc/orders.md#searchorders)

### Structure

`ListRefundsRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `begin_time` | `String` | Optional | The beginning of the requested reporting period, in RFC 3339 format.<br><br>See [Date ranges](#dateranges) for details on date inclusivity/exclusivity.<br><br>Default value: The current time minus one year. |
| `end_time` | `String` | Optional | The end of the requested reporting period, in RFC 3339 format.<br><br>See [Date ranges](#dateranges) for details on date inclusivity/exclusivity.<br><br>Default value: The current time. |
| `sort_order` | [`String (Sort Order)`](/doc/models/sort-order.md) | Optional | The order (e.g., chronological or alphabetical) in which results from a request are returned. |
| `cursor` | `String` | Optional | A pagination cursor returned by a previous call to this endpoint.<br>Provide this to retrieve the next set of results for your original query.<br><br>See [Pagination](https://developer.squareup.com/docs/basics/api101/pagination) for more information. |

### Example (as JSON)

```json
{
  "begin_time": null,
  "end_time": null,
  "sort_order": null,
  "cursor": null
}
```

