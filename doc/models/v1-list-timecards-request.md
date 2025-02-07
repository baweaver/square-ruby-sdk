## V1 List Timecards Request

### Structure

`V1ListTimecardsRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order` | [`String (Sort Order)`](/doc/models/sort-order.md) | Optional | The order (e.g., chronological or alphabetical) in which results from a request are returned. |
| `employee_id` | `String` | Optional | If provided, the endpoint returns only timecards for the employee with the specified ID. |
| `begin_clockin_time` | `String` | Optional | If filtering results by their clockin_time field, the beginning of the requested reporting period, in ISO 8601 format. |
| `end_clockin_time` | `String` | Optional | If filtering results by their clockin_time field, the end of the requested reporting period, in ISO 8601 format. |
| `begin_clockout_time` | `String` | Optional | If filtering results by their clockout_time field, the beginning of the requested reporting period, in ISO 8601 format. |
| `end_clockout_time` | `String` | Optional | If filtering results by their clockout_time field, the end of the requested reporting period, in ISO 8601 format. |
| `begin_updated_at` | `String` | Optional | If filtering results by their updated_at field, the beginning of the requested reporting period, in ISO 8601 format. |
| `end_updated_at` | `String` | Optional | If filtering results by their updated_at field, the end of the requested reporting period, in ISO 8601 format. |
| `deleted` | `Boolean` | Optional | If true, only deleted timecards are returned. If false, only valid timecards are returned.If you don't provide this parameter, both valid and deleted timecards are returned. |
| `limit` | `Integer` | Optional | The maximum integer number of employee entities to return in a single response. Default 100, maximum 200. |
| `batch_token` | `String` | Optional | A pagination cursor to retrieve the next set of results for your<br>original query to the endpoint. |

### Example (as JSON)

```json
{
  "order": null,
  "employee_id": null,
  "begin_clockin_time": null,
  "end_clockin_time": null,
  "begin_clockout_time": null,
  "end_clockout_time": null,
  "begin_updated_at": null,
  "end_updated_at": null,
  "deleted": null,
  "limit": null,
  "batch_token": null
}
```

