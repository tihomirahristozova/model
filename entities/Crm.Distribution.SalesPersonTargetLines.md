# Crm.Distribution.SalesPersonTargetLines

Detail records (lines) of targets for sales persons. Entity: Crm_Sales_Person_Target_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Distribution.SalesPersonTargetLines.md#Id) | guid |  
| [PeriodDate](Crm.Distribution.SalesPersonTargetLines.md#PeriodDate) | datetime | Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes). [Required] [ReadOnly] 
| [PeriodMonth](Crm.Distribution.SalesPersonTargetLines.md#PeriodMonth) | byte | Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). [Required] [Filter(ge;le)] 
| [PeriodYear](Crm.Distribution.SalesPersonTargetLines.md#PeriodYear) | int16 | Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). [Required] [Filter(ge;le)] 
| [TargetAmount](Crm.Distribution.SalesPersonTargetLines.md#TargetAmount) | [Amount](../data-types/Amount.md) (nullable) | Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value. [Currency: TargetAmountCurrency] 
| [TargetType](Crm.Distribution.SalesPersonTargetLines.md#TargetType) | [Crm.Distribution.SalesPersonTargetLinesRepository.TargetType](Crm.Distribution.SalesPersonTargetLines.md#TargetType) | Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs. [Required] [Default("SALES")] [Filter(multi eq)] 
| [TargetValue](Crm.Distribution.SalesPersonTargetLines.md#TargetValue) | decimal | Value of target. Meaning depends on target type. [Required] [Default(0)] 
| [TargetWeight](Crm.Distribution.SalesPersonTargetLines.md#TargetWeight) | decimal | Relative weight of target, comparatively to other targets. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BonusProgram](Crm.Distribution.SalesPersonTargetLines.md#BonusProgram) | [Crm.Marketing.BonusPrograms](Crm.Marketing.BonusPrograms.md) (nullable) | Bonus program Id when the target type is BONUS, null otherwise. [Filter(multi eq)] |
| [ProductGroup](Crm.Distribution.SalesPersonTargetLines.md#ProductGroup) | [General.Products.ProductGroups](General.Products.ProductGroups.md) (nullable) | Product group for which the target is defined. [Filter(multi eq)] |
| [PromotionalPackage](Crm.Distribution.SalesPersonTargetLines.md#PromotionalPackage) | [Crm.PromotionalPackages](Crm.PromotionalPackages.md) (nullable) | Promotional Package Id when the target type is PROMO, null otherwise. [Filter(multi eq)] |
| [SalesPerson](Crm.Distribution.SalesPersonTargetLines.md#SalesPerson) | [Crm.SalesPersons](Crm.SalesPersons.md) | Sales person to whom the target is assigned. [Required] [Filter(multi eq)] |
| [SalesPersonTarget](Crm.Distribution.SalesPersonTargetLines.md#SalesPersonTarget) | [Crm.Distribution.SalesPersonTargets](Crm.Distribution.SalesPersonTargets.md) | The [SalesPersonTarget](Crm.Distribution.SalesPersonTargetLines.md#SalesPersonTarget) to which this SalesPersonTargetLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [TargetAmountCurrency](Crm.Distribution.SalesPersonTargetLines.md#TargetAmountCurrency) | [General.Currencies](General.Currencies.md) (nullable) | Deprecated - use currency in document header. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### PeriodDate

> Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes). [Required] [ReadOnly]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PeriodMonth

> Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). [Required] [Filter(ge;le)]

_Type_: **byte**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PeriodYear

> Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). [Required] [Filter(ge;le)]

_Type_: **int16**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### TargetAmount

> Target amount to be fulfilled by the specified sales person. Deprecated - use Target_Value. [Currency: TargetAmountCurrency]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TargetType

> Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs. [Required] [Default("SALES")] [Filter(multi eq)]

_Type_: **[Crm.Distribution.SalesPersonTargetLinesRepository.TargetType](Crm.Distribution.SalesPersonTargetLines.md#TargetType)**  
Allowed values for the [TargetType](Crm.Distribution.SalesPersonTargetLines.md#TargetType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| SalesAmount | SalesAmount value. Stored as 'SALES'. <br /> _Database Value:_ 'SALES' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SalesAmount' |
| NumberOfAppliedBonusPrograms | NumberOfAppliedBonusPrograms value. Stored as 'BONUS'. <br /> _Database Value:_ 'BONUS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NumberOfAppliedBonusPrograms' |
| NumberOfPromotionalPackages | NumberOfPromotionalPackages value. Stored as 'PROMO'. <br /> _Database Value:_ 'PROMO' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'NumberOfPromotionalPackages' |
| LocationsCount | LocationsCount value. Stored as 'LOCNT'. <br /> _Database Value:_ 'LOCNT' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'LocationsCount' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **SalesAmount**  

### TargetValue

> Value of target. Meaning depends on target type. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### TargetWeight

> Relative weight of target, comparatively to other targets. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### BonusProgram

> Bonus program Id when the target type is BONUS, null otherwise. [Filter(multi eq)]

_Type_: **[Crm.Marketing.BonusPrograms](Crm.Marketing.BonusPrograms.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductGroup

> Product group for which the target is defined. [Filter(multi eq)]

_Type_: **[General.Products.ProductGroups](General.Products.ProductGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesPersonTarget.ProductGroup`

_Front-End Recalc Expressions:_  
`obj.SalesPersonTarget.ProductGroup`
### PromotionalPackage

> Promotional Package Id when the target type is PROMO, null otherwise. [Filter(multi eq)]

_Type_: **[Crm.PromotionalPackages](Crm.PromotionalPackages.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SalesPerson

> Sales person to whom the target is assigned. [Required] [Filter(multi eq)]

_Type_: **[Crm.SalesPersons](Crm.SalesPersons.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesPersonTarget.SalesPerson`

_Front-End Recalc Expressions:_  
`obj.SalesPersonTarget.SalesPerson`
### SalesPersonTarget

> The [SalesPersonTarget](Crm.Distribution.SalesPersonTargetLines.md#SalesPersonTarget) to which this SalesPersonTargetLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Distribution.SalesPersonTargets](Crm.Distribution.SalesPersonTargets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TargetAmountCurrency

> Deprecated - use currency in document header. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SalesPersonTarget.TargetCurrency`

_Front-End Recalc Expressions:_  
`obj.SalesPersonTarget.TargetCurrency`


## Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonTargetLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Distribution.SalesPersonTargetLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Distribution.SalesPersonTargetLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Distribution_SalesPersonTargetLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Distribution_SalesPersonTargetLines?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_Person_Target_Lines?$top=10>

