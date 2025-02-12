## List Employee Wages Request

A request for a set of `EmployeeWage` objects

### Structure

`ListEmployeeWagesRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `employee_id` | `String` | Optional | Filter wages returned to only those that are associated with the<br>specified employee. |
| `limit` | `Integer` | Optional | Maximum number of Employee Wages to return per page. Can range between<br>1 and 200. The default is the maximum at 200. |
| `cursor` | `String` | Optional | Pointer to the next page of Employee Wage results to fetch. |

### Example (as JSON)

```json
{
  "employee_id": null,
  "limit": null,
  "cursor": null
}
```

