## Update Break Type Request

A request to update a `BreakType`

### Structure

`UpdateBreakTypeRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `break_type` | [`Break Type Hash`](/doc/models/break-type.md) | Optional | A defined break template that sets an expectation for possible `Break` <br>instances on a `Shift`. |

### Example (as JSON)

```json
{
  "break_type": {
    "location_id": "26M7H24AZ9N6R",
    "break_name": "Lunch",
    "expected_duration": "PT50M",
    "is_paid": true,
    "version": 1
  }
}
```

