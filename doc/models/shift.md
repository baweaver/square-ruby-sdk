## Shift

A record of the hourly rate, start, and end times for a single work shift 
for an employee. May include a record of the start and end times for breaks 
taken during the shift.

### Structure

`Shift`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | UUID for this object |
| `employee_id` | `String` |  | The ID of the employee this shift belongs to. |
| `location_id` | `String` | Optional | The ID of the location this shift occurred at. Should be based on<br>where the employee clocked in. |
| `timezone` | `String` | Optional | Read-only convenience value that is calculated from the location based<br>on `location_id`. Format: the IANA Timezone Database identifier for the<br>location timezone. |
| `start_at` | `String` |  | RFC 3339; shifted to location timezone + offset. Precision up to the<br>minute is respected; seconds are truncated. |
| `end_at` | `String` | Optional | RFC 3339; shifted to timezone + offset. Precision up to the minute is<br>respected; seconds are truncated. The `end_at` minute is not<br>counted when the shift length is calculated. For example, a shift from `00:00`<br>to `08:01` is considered an 8 hour shift (midnight to 8am). |
| `wage` | [`Shift Wage Hash`](/doc/models/shift-wage.md) | Optional | The hourly wage rate used to compensate an employee for this shift. |
| `breaks` | [`Array<Break Hash>`](/doc/models/break.md) | Optional | A list of any paid or unpaid breaks that were taken during this shift. |
| `status` | [`String (Shift Status)`](/doc/models/shift-status.md) | Optional | Enumerates the possible status of a `Shift` |
| `version` | `Integer` | Optional | Used for resolving concurrency issues; request will fail if version<br>provided does not match server version at time of request. If not provided,<br>Square executes a blind write; potentially overwriting data from another<br>write. |
| `created_at` | `String` | Optional | A read-only timestamp in RFC 3339 format; presented in UTC. |
| `updated_at` | `String` | Optional | A read-only timestamp in RFC 3339 format; presented in UTC. |

### Example (as JSON)

```json
{
  "id": null,
  "employee_id": "employee_id0",
  "location_id": null,
  "timezone": null,
  "start_at": "start_at2",
  "end_at": null,
  "wage": null,
  "breaks": null,
  "status": null,
  "version": null,
  "created_at": null,
  "updated_at": null
}
```

