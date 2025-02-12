## Retrieve Customer Response

Defines the fields that are included in the response body of
a request to the RetrieveCustomer endpoint.

One of `errors` or `customer` is present in a given response (never both).

### Structure

`RetrieveCustomerResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | Any errors that occurred during the request. |
| `customer` | [`Customer Hash`](/doc/models/customer.md) | Optional | Represents one of a business's customers, which can have one or more<br>cards on file associated with it. |

### Example (as JSON)

```json
{
  "customer": {
    "id": "JDKYHBWT1D4F8MFH63DBMEN8Y4",
    "created_at": "2016-03-23T20:21:54.859Z",
    "updated_at": "2016-03-23T20:21:54.859Z",
    "given_name": "Amelia",
    "family_name": "Earhart",
    "email_address": "Amelia.Earhart@example.com",
    "address": {
      "address_line_1": "500 Electric Ave",
      "address_line_2": "Suite 600",
      "locality": "New York",
      "administrative_district_level_1": "NY",
      "postal_code": "10003",
      "country": "US"
    },
    "phone_number": "1-212-555-4240",
    "reference_id": "YOUR_REFERENCE_ID",
    "note": "a customer",
    "groups": [
      {
        "id": "16894e93-96eb-4ced-b24b-f71d42bf084c",
        "name": "Aviation Enthusiasts"
      }
    ]
  }
}
```

