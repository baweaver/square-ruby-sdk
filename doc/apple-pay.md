# Apple Pay

```ruby
apple_pay_api = client.apple_pay
```

## Class Name

`ApplePayApi`

## Register Domain

Activates a domain for use with Web Apple Pay and Square. A validation
will be performed on this domain by Apple to ensure is it properly set up as
an Apple Pay enabled domain.

This endpoint provides an easy way for platform developers to bulk activate
Web Apple Pay with Square for merchants using their platform.

To learn more about Apple Pay on Web see the Apple Pay section in the
[Embedding the Square Payment Form](/payment-form/add-digital-wallets/apple-pay) guide.

```ruby
def register_domain(body:)
```

### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Register Domain Request Hash`](/doc/models/register-domain-request.md) | Body, Required | An object containing the fields to POST for the request.<br><br>See the corresponding object definition for field details. |

### Response Type

[`Register Domain Response Hash`](/doc/models/register-domain-response.md)

### Example Usage

```ruby
body = {}
body[:domain_name] = 'example.com'

result = apple_pay_api.register_domain(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

