---
uid: General.DocumentAmounts
---
# General.DocumentAmounts Entity

**Namespace:** [General](General.md)  

Contains a specific instance of an additional amount for a specific document. Entity: Gen_Document_Amounts

## Default Visualization
Default Display Text Format:  
_{Document.EntityName}_  
Default Search Members:  
_Document.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Documents](General.Documents.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseAmount](General.DocumentAmounts.md#baseamount) | [Amount (14, 2)](../data-types.md#amount) __nullable__ | The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet. `Currency: LogisticsDocument.DocumentCurrency` `ReadOnly` 
| [Id](General.DocumentAmounts.md#id) | guid |  
| [InputAmount](General.DocumentAmounts.md#inputamount) | [Amount (14, 2)](../data-types.md#amount) __nullable__ | When not null, specifies directly the amount of the additional amount. `Currency: GetInputAmountCurrency()` `Filter(ge;le)` 
| [InputPercent](General.DocumentAmounts.md#inputpercent) | decimal (7, 6) __nullable__ | When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type). `Filter(ge;le)` 
| [InputUnitAmount](General.DocumentAmounts.md#inputunitamount) | [Amount (14, 5)](../data-types.md#amount) __nullable__ | Input unit amount for the calculation of the current amount. `Currency: GetInputAmountCurrency()` `Filter(eq;ge;le)` 
| [RowVersion](General.DocumentAmounts.md#rowversion) | byte[] |  
| [TotalDistributedAmount](General.DocumentAmounts.md#totaldistributedamount) | [Amount (14, 2)](../data-types.md#amount) __nullable__ | The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet. `Currency: LogisticsDocument.DocumentCurrency` `ReadOnly` 
| [UserCanChangeInput](General.DocumentAmounts.md#usercanchangeinput) | boolean | True if the user, entering the document is allowed to change the default input percent. `Required` `Default(true)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentAmounts.md#document) | [Documents](General.Documents.md) | The <see cref="Document"/> to which this DocumentAmount belongs. `Required` `Filter(multi eq)` `Owner` |
| [DocumentAmountType](General.DocumentAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The type of the amount. `Required` `Filter(multi eq)` |
| [InputAmountCurrency](General.DocumentAmounts.md#inputamountcurrency) | [Currencies](General.Currencies.md) (nullable) | When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null. `Filter(multi eq)` |
| [InputUnit](General.DocumentAmounts.md#inputunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | Measurement unit of the input unit amount. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ReferencedDocuments | [DocumentAmountReferencedDocuments](General.DocumentAmountReferencedDocuments.md) | List of `DocumentAmount<br />ReferencedDocument`(General.DocumentAmount<br />ReferencedDocuments.md) child objects, based on the `General.DocumentAmount<br />ReferencedDocument.DocumentAmount`(General.DocumentAmount<br />ReferencedDocuments.md#documentamount) back reference 


## Attribute Details

### BaseAmount

The calculated base amount (in documents currency) from the last document amount recalculation. The base amount is the base, over which the additional amounts are calculated. Null if the amount is not distributed yet. `Currency: LogisticsDocument.DocumentCurrency` `ReadOnly`

_Type_: **[Amount (14, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### InputAmount

When not null, specifies directly the amount of the additional amount. `Currency: GetInputAmountCurrency()` `Filter(ge;le)`

_Type_: **[Amount (14, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( obj.DocumentAmountType.AmountInputAllowed, obj.InputAmount, null)`
### InputPercent

When not null, specifies that the amount for this document will be calculated as percent of the base amounts (which are defined in the amount type). `Filter(ge;le)`

_Type_: **decimal (7, 6) __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.DocumentAmountType.DefaultPercent`

_Front-End Recalc Expressions:_  
`obj.DocumentAmountType.DefaultPercent`
### InputUnitAmount

Input unit amount for the calculation of the current amount. `Currency: GetInputAmountCurrency()` `Filter(eq;ge;le)`

_Type_: **[Amount (14, 5)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( obj.DocumentAmountType.UnitAmountInputAllowed, obj.InputUnitAmount, null)`
### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TotalDistributedAmount

The total amount (in documents currency) which was distributed to the documents lines. Null if the amount is not distributed yet. `Currency: LogisticsDocument.DocumentCurrency` `ReadOnly`

_Type_: **[Amount (14, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UserCanChangeInput

True if the user, entering the document is allowed to change the default input percent. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  


## Reference Details

### Document

The <see cref="Document"/> to which this DocumentAmount belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### DocumentAmountType

The type of the amount. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### InputAmountCurrency

When specifying the amount directly in Input Amount, this contains the currency of the amount. Used and required when Input Amount is not null. `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( obj.DocumentAmountType.AmountInputAllowed, obj.InputAmountCurrency, null)`
### InputUnit

Measurement unit of the input unit amount. `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( obj.DocumentAmountType.UnitAmountInputAllowed, obj.InputUnit, null)`


## Business Rules

[!list limit=1000 erp.entity=General.DocumentAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmounts?$top=10>

