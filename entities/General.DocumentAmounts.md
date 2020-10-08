---
uid: General.DocumentAmounts
---
# General.DocumentAmounts

Contains a specific instance of an additional amount for a specific document. Entity: Gen_Document_Amounts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentAmounts.md#Id) | guid |  
| [BaseAmount](General.DocumentAmounts.md#BaseAmount) | [Amount](../data-types.md#Amount) (nullable) | The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet. [Currency: LogisticsDocument.DocumentCurrency] [ReadOnly] 
| [InputAmount](General.DocumentAmounts.md#InputAmount) | [Amount](../data-types.md#Amount) (nullable) | When not null, specifies directly the amount of the additional amount. [Currency: GetInputAmountCurrency()] [Filter(ge;le)] 
| [InputPercent](General.DocumentAmounts.md#InputPercent) | decimal (nullable) | When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type). [Filter(ge;le)] 
| [InputUnitAmount](General.DocumentAmounts.md#InputUnitAmount) | [Amount](../data-types.md#Amount) (nullable) | Input unit amount for the calculation of the current amount. [Currency: GetInputAmountCurrency()] [Filter(eq;ge;le)] 
| [TotalDistributedAmount](General.DocumentAmounts.md#TotalDistributedAmount) | [Amount](../data-types.md#Amount) (nullable) | The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet. [Currency: LogisticsDocument.DocumentCurrency] [ReadOnly] 
| [UserCanChangeInput](General.DocumentAmounts.md#UserCanChangeInput) | boolean | True if the user, entering the document is allowed to change the default input percent. [Required] [Default(true)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmountType](General.DocumentAmounts.md#DocumentAmountType) | [General.DocumentAmountTypes](General.DocumentAmountTypes.md) | The type of the amount. [Required] [Filter(multi eq)] |
| [Document](General.DocumentAmounts.md#Document) | [General.Documents](General.Documents.md) | The [Document](General.DocumentAmounts.md#Document) to which this DocumentAmount belongs. [Required] [Filter(multi eq)] [Owner] |
| [InputAmountCurrency](General.DocumentAmounts.md#InputAmountCurrency) | [General.Currencies](General.Currencies.md) (nullable) | When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null. [Filter(multi eq)] |
| [InputUnit](General.DocumentAmounts.md#InputUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) (nullable) | Measurement unit of the input unit amount. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ReferencedDocuments | [General.DocumentAmountReferencedDocuments](General.DocumentAmountReferencedDocuments.md) | List of [DocumentAmountReferencedDocument](General.DocumentAmountReferencedDocuments.md) child objects, based on the [General.DocumentAmountReferencedDocument.DocumentAmount](General.DocumentAmountReferencedDocuments.md#DocumentAmount) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BaseAmount

> The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet. [Currency: LogisticsDocument.DocumentCurrency] [ReadOnly]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### InputAmount

> When not null, specifies directly the amount of the additional amount. [Currency: GetInputAmountCurrency()] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(obj.DocumentAmountType.AmountInputAllowed, obj.InputAmount, null)`
### InputPercent

> When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type). [Filter(ge;le)]

_Type_: **decimal (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.DocumentAmountType.DefaultPercent`

_Front-End Recalc Expressions:_  
`obj.DocumentAmountType.DefaultPercent`
### InputUnitAmount

> Input unit amount for the calculation of the current amount. [Currency: GetInputAmountCurrency()] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(obj.DocumentAmountType.UnitAmountInputAllowed, obj.InputUnitAmount, null)`
### TotalDistributedAmount

> The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet. [Currency: LogisticsDocument.DocumentCurrency] [ReadOnly]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UserCanChangeInput

> True if the user, entering the document is allowed to change the default input percent. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  


## Reference Details

### DocumentAmountType

> The type of the amount. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Document

> The [Document](General.DocumentAmounts.md#Document) to which this DocumentAmount belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### InputAmountCurrency

> When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(obj.DocumentAmountType.AmountInputAllowed, obj.InputAmountCurrency, null)`
### InputUnit

> Measurement unit of the input unit amount. [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(obj.DocumentAmountType.UnitAmountInputAllowed, obj.InputUnit, null)`


## Business Rules

[!list erp.entity=General.DocumentAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentAmounts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentAmounts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmounts?$top=10>

