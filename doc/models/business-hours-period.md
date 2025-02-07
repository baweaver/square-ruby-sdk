## Business Hours Period

Represents a period of time during which a business location is open.

### Structure

`BusinessHoursPeriod`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `day_of_week` | [`String (Day of Week)`](/doc/models/day-of-week.md) | Optional | Indicates the specific day  of the week. |
| `start_local_time` | `String` | Optional | The start time of a business hours period, specified in local time using partial-time<br>RFC3339 format. |
| `end_local_time` | `String` | Optional | The end time of a business hours period, specified in local time using partial-time<br>RFC3339 format. |

### Example (as JSON)

```json
{
  "day_of_week": null,
  "start_local_time": null,
  "end_local_time": null
}
```

