---
uid: Crm.DiscountTypes
---
# Crm.DiscountTypes

Contains the different types of discounts, which can be applied to sales lines. Different types of discounts can be combined for a single sales line. Entity: Crm_Discount_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.DiscountTypes.md#Id) | guid |  
| [ActionType](Crm.DiscountTypes.md#ActionType) | [Crm.DiscountTypesRepository.ActionType](Crm.DiscountTypes.md#ActionType) | Specifies the way the discount is applied over the previous discounts. [Required] [Default("A")] [Filter(multi eq)] 
| [CalculationMethod](Crm.DiscountTypes.md#CalculationMethod) | [Crm.DiscountTypesRepository.CalculationMethod](Crm.DiscountTypes.md#CalculationMethod) | Specifies whether the calculation method of the discount is based on a standard discount, promotional package, bonus program, etc. [Required] [Filter(multi eq)] 
| [Code](Crm.DiscountTypes.md#Code) | string | The unique code of the DiscountType. [Required] [Filter(eq)] 
| [Name](Crm.DiscountTypes.md#Name) | string | The name of this DiscountType. [Required] [Filter(like)] 
| [IsSystem](Crm.DiscountTypes.md#IsSystem) | boolean | Specifies whether this discount type is created and managed by the system. [Required] [Default(false)] [Filter(multi eq)] 
| [Notes](Crm.DiscountTypes.md#Notes) | string (nullable) | Notes for this DiscountType. 
| [Ord](Crm.DiscountTypes.md#Ord) | int32 | Determines the order in which the discounts are applied. The discounts with smaller Ord are applied first. [Required] [Default(1)] [Filter(ge;le)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ActionType

> Specifies the way the discount is applied over the previous discounts. [Required] [Default("A")] [Filter(multi eq)]

_Type_: **[Crm.DiscountTypesRepository.ActionType](Crm.DiscountTypes.md#ActionType)**  
Allowed values for the [ActionType](Crm.DiscountTypes.md#ActionType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Add | Add value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Add' |
| Replace | Replace value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Replace' |
| MarkDown | MarkDown value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MarkDown' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Add**  

### CalculationMethod

> Specifies whether the calculation method of the discount is based on a standard discount, promotional package, bonus program, etc. [Required] [Filter(multi eq)]

_Type_: **[Crm.DiscountTypesRepository.CalculationMethod](Crm.DiscountTypes.md#CalculationMethod)**  
Allowed values for the [CalculationMethod](Crm.DiscountTypes.md#CalculationMethod) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| StandardDiscount | StandardDiscount value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'StandardDiscount' |
| PromotionalPackage | PromotionalPackage value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'PromotionalPackage' |
| BonusProgram | BonusProgram value. Stored as 'B'. <br /> _Database Value:_ 'B' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BonusProgram' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Code

> The unique code of the DiscountType. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Name

> The name of this DiscountType. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### IsSystem

> Specifies whether this discount type is created and managed by the system. [Required] [Default(false)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes for this DiscountType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Ord

> Determines the order in which the discounts are applied. The discounts with smaller Ord are applied first. [Required] [Default(1)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  



## Business Rules

[!list erp.entity=Crm.DiscountTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.DiscountTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.DiscountTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_DiscountTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_DiscountTypes?$top=10>

