## Order Line Item Tax Scope

Indicates whether this is a line item or order level tax.

### Enumeration

`OrderLineItemTaxScope`

### Fields

| Name | Description |
|  --- | --- |
| `OTHER_TAX_SCOPE` | Used for reporting only.<br>The original transaction tax scope is currently not supported by the API. |
| `LINE_ITEM` | The tax should be applied to only line items specified by `OrderLineItemAppliedTax`<br>reference records. |
| `ORDER` | The tax should be applied to the entire order. |

