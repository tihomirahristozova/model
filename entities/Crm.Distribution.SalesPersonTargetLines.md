---
uid: Crm.Distribution.SalesPersonTargetLines
---
# Crm.Distribution.SalesPersonTargetLines Entity

**Namespace:** [Crm.Distribution](Crm.Distribution.md)  

Detail records (lines) of targets for sales persons. Entity: Crm_Sales_Person_Target_Lines

## Default Visualization
Default Display Text Format:  
_{SalesPersonTarget.DocumentType.Code}:{SalesPersonTarget.DocumentNo} - {SalesPersonTarget.DocumentType.TypeName:T}_  
Default Search Member:  
_SalesPersonTarget.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Distribution.SalesPersonTargets](Crm.Distribution.SalesPersonTargets.md)  
Aggregate Root:  
[Crm.Distribution.SalesPersonTargets](Crm.Distribution.SalesPersonTargets.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Distribution.SalesPersonTargetLines.md#id) | guid |  
| [PeriodDate](Crm.Distribution.SalesPersonTargetLines.md#perioddate) | datetime | Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes). `Required` `ReadOnly` 
| [PeriodMonth](Crm.Distribution.SalesPersonTargetLines.md#periodmonth) | byte | Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). `Required` `Filter(ge;le)` 
| [PeriodYear](Crm.Distribution.SalesPersonTargetLines.md#periodyear) | int16 | Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). `Required` `Filter(ge;le)` 
| [TargetAmount](Crm.Distribution.SalesPersonTargetLines.md#targetamount) | [Amount (18, 2)](../data-types.md#amount) __nullable__ | Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value. `Currency: TargetAmountCurrency` 
| [TargetType](Crm.Distribution.SalesPersonTargetLines.md#targettype) | [TargetType](Crm.Distribution.SalesPersonTargetLines.md#targettype) | Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs. `Required` `Default("SALES")` `Filter(multi eq)` 
| [TargetValue](Crm.Distribution.SalesPersonTargetLines.md#targetvalue) | decimal (9, 2) | Value of target. Meaning depends on target type. `Required` `Default(0)` 
| [TargetWeight](Crm.Distribution.SalesPersonTargetLines.md#targetweight) | decimal (5, 2) | Relative weight of target, comparatively to other targets. `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BonusProgram](Crm.Distribution.SalesPersonTargetLines.md#bonusprogram) | [BonusPrograms](Crm.Marketing.BonusPrograms.md) (nullable) | Bonus program Id when the target type is BONUS, null otherwise. `Filter(multi eq)` |
| [ProductGroup](Crm.Distribution.SalesPersonTargetLines.md#productgroup) | [ProductGroups](General.Products.ProductGroups.md) (nullable) | Product group for which the target is defined. `Filter(multi eq)` |
| [PromotionalPackage](Crm.Distribution.SalesPersonTargetLines.md#promotionalpackage) | [PromotionalPackages](Crm.PromotionalPackages.md) (nullable) | Promotional Package Id when the target type is PROMO, null otherwise. `Filter(multi eq)` |
| [SalesPerson](Crm.Distribution.SalesPersonTargetLines.md#salesperson) | [SalesPersons](Crm.SalesPersons.md) | Sales person to whom the target is assigned. `Required` `Filter(multi eq)` |
| [SalesPersonTarget](Crm.Distribution.SalesPersonTargetLines.md#salespersontarget) | [SalesPersonTargets](Crm.Distribution.SalesPersonTargets.md) | The `SalesPersonTarget`(Crm.Distribution.SalesPersonTargetLines.md#salespersontarget) to which this SalesPersonTargetLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [TargetAmountCurrency](Crm.Distribution.SalesPersonTargetLines.md#targetamountcurrency) | [Currencies](General.Currencies.md) (nullable) | Deprecated - use currency in document header. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### PeriodDate

Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes). `Required` `ReadOnly`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PeriodMonth

Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). `Required` `Filter(ge;le)`

_Type_: **byte**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PeriodYear

Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). `Required` `Filter(ge;le)`

_Type_: **int16**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### TargetAmount

Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value. `Currency: TargetAmountCurrency`

_Type_: **[Amount (18, 2)](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TargetType

Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs. `Required` `Default("SALES")` `Filter(multi eq)`

_Type_: **[TargetType](Crm.Distribution.SalesPersonTargetLines.md#targettype)**  
Allowed values for the `TargetType`(Crm.Distribution.SalesPersonTargetLines.md#targettype) data attribute  
_Allowed Values (Crm.Distribution.SalesPersonTargetLinesRepository.TargetType Enum Members)_  

| Value | Description |
| ---- | --- |
| SalesAmount | SalesAmount value. Stored as 'SALES'. <br /> _Database Value:_ 'SALES' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SalesAmount' |
| NumberOfApplied<br />BonusPrograms | NumberOfApplied<br />BonusPrograms value. Stored as 'BONUS'. <br /> _Database Value:_ 'BONUS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NumberOfApplied<br />BonusPrograms' |
| NumberOfPromotional<br />Packages | NumberOfPromotional<br />Packages value. Stored as 'PROMO'. <br /> _Database Value:_ 'PROMO' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'NumberOfPromotional<br />Packages' |
| LocationsCount | LocationsCount value. Stored as 'LOCNT'. <br /> _Database Value:_ 'LOCNT' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'LocationsCount' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **SalesAmount**  

### TargetValue

Value of target. Meaning depends on target type. `Required` `Default(0)`

_Type_: **decimal (9, 2)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### TargetWeight

Relative weight of target, comparatively to other targets. `Required` `Default(1)`

_Type_: **decimal (5, 2)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### BonusProgram

Bonus program Id when the target type is BONUS, null otherwise. `Filter(multi eq)`

_Type_: **[BonusPrograms](Crm.Marketing.BonusPrograms.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductGroup

Product group for which the target is defined. `Filter(multi eq)`

_Type_: **[ProductGroups](General.Products.ProductGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SalesPersonTarget.ProductGroup`

_Front-End Recalc Expressions:_  
`obj.SalesPersonTarget.ProductGroup`
### PromotionalPackage

Promotional Package Id when the target type is PROMO, null otherwise. `Filter(multi eq)`

_Type_: **[PromotionalPackages](Crm.PromotionalPackages.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SalesPerson

Sales person to whom the target is assigned. `Required` `Filter(multi eq)`

_Type_: **[SalesPersons](Crm.SalesPersons.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SalesPersonTarget.SalesPerson`

_Front-End Recalc Expressions:_  
`obj.SalesPersonTarget.SalesPerson`
### SalesPersonTarget

The `SalesPersonTarget`(Crm.Distribution.SalesPersonTargetLines.md#salespersontarget) to which this SalesPersonTargetLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[SalesPersonTargets](Crm.Distribution.SalesPersonTargets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TargetAmountCurrency

Deprecated - use currency in document header. `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SalesPersonTarget.TargetCurrency`

_Front-End Recalc Expressions:_  
`obj.SalesPersonTarget.TargetCurrency`


## Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonTargetLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonTargetLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Distribution_SalesPersonTargetLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Distribution_SalesPersonTargetLines?$top=10>

