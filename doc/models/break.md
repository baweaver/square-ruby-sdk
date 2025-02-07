## Break

A record of an employee's break during a shift.

### Structure

`Break`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | UUID for this object |
| `start_at` | `String` |  | RFC 3339; follows same timezone info as `Shift`. Precision up to<br>the minute is respected; seconds are truncated. |
| `end_at` | `String` | Optional | RFC 3339; follows same timezone info as `Shift`. Precision up to<br>the minute is respected; seconds are truncated. The `end_at` minute is not<br>counted when the break length is calculated. For example, a break from `00:00`<br>to `00:11`  is considered a 10 minute break (midnight to 10 minutes after midnight). |
| `break_type_id` | `String` |  | The `BreakType` this `Break` was templated on. |
| `name` | `String` |  | A human-readable name. |
| `expected_duration` | `String` |  | Format: RFC-3339 P[n]Y[n]M[n]DT[n]H[n]M[n]S. The expected length of<br>the break. |
| `is_paid` | `Boolean` |  | Whether this break counts towards time worked for compensation<br>purposes. |

### Example (as JSON)

```json
{
  "id": null,
  "start_at": "start_at2",
  "end_at": null,
  "break_type_id": "break_type_id6",
  "name": "name0",
  "expected_duration": "expected_duration4",
  "is_paid": false
}
```

