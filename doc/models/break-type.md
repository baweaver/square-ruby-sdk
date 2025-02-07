## Break Type

A defined break template that sets an expectation for possible `Break` 
instances on a `Shift`.

### Structure

`BreakType`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | UUID for this object. |
| `location_id` | `String` |  | The ID of the business location this type of break applies to. |
| `break_name` | `String` |  | A human-readable name for this type of break. Will be displayed to<br>employees in Square products. |
| `expected_duration` | `String` |  | Format: RFC-3339 P[n]Y[n]M[n]DT[n]H[n]M[n]S. The expected length of<br>this break. Precision below minutes is truncated. |
| `is_paid` | `Boolean` |  | Whether this break counts towards time worked for compensation<br>purposes. |
| `version` | `Integer` | Optional | Used for resolving concurrency issues; request will fail if version<br>provided does not match server version at time of request. If a value is not<br>provided, Square's servers execute a "blind" write; potentially <br>overwriting another writer's data. |
| `created_at` | `String` | Optional | A read-only timestamp in RFC 3339 format. |
| `updated_at` | `String` | Optional | A read-only timestamp in RFC 3339 format. |

### Example (as JSON)

```json
{
  "id": null,
  "location_id": "location_id4",
  "break_name": "break_name8",
  "expected_duration": "expected_duration4",
  "is_paid": false,
  "version": null,
  "created_at": null,
  "updated_at": null
}
```

