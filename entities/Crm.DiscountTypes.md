---
uid: Crm.DiscountTypes
---
# Crm.DiscountTypes Entity

**Namespace:** [Crm](Crm.md)  

Contains the different types of discounts, which can be applied to sales lines. Different types of discounts can be combined for a single sales line. Entity: Crm_Discount_Types

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [Crm.DiscountTypes](Crm.DiscountTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ActionType](Crm.DiscountTypes.md#actiontype) | [ActionType](Crm.DiscountTypes.md#actiontype) | Specifies the way the discount is applied over the previous discounts. [Required] [Default("A")] [Filter(multi eq)] 
| [CalculationMethod](Crm.DiscountTypes.md#calculationmethod) | [CalculationMethod](Crm.DiscountTypes.md#calculationmethod) | Specifies whether the calculation method of the discount is based on a standard discount, promotional package, bonus program, etc. [Required] [Filter(multi eq)] 
| [Code](Crm.DiscountTypes.md#code) | string | The unique code of the DiscountType. [Required] [Filter(eq)] 
| [Id](Crm.DiscountTypes.md#id) | guid |  
| [IsSystem](Crm.DiscountTypes.md#issystem) | boolean | Specifies whether this discount type is created and managed by the system. [Required] [Default(false)] [Filter(multi eq)] 
| [Name](Crm.DiscountTypes.md#name) | string | The name of this DiscountType. [Required] [Filter(like)] 
| [Notes](Crm.DiscountTypes.md#notes) | string (nullable) | Notes for this DiscountType. 
| [Ord](Crm.DiscountTypes.md#ord) | int32 | Determines the order in which the discounts are applied. The discounts with smaller Ord are applied first. [Required] [Default(1)] [Filter(ge;le)] 


## Attribute Details

### ActionType

Specifies the way the discount is applied over the previous discounts. [Required] [Default("A")] [Filter(multi eq)]

_Type_: **[ActionType](Crm.DiscountTypes.md#actiontype)**  
Allowed values for the [ActionType](Crm.DiscountTypes.md#actiontype) data attribute  
_Allowed Values (Crm.DiscountTypesRepository.ActionType Enum Members)_  

| Value | Description |
| ---- | --- |
| Add | Add value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Add' |
| Replace | Replace value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Replace' |
| MarkDown | MarkDown value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MarkDown' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Add**  

### CalculationMethod

Specifies whether the calculation method of the discount is based on a standard discount, promotional package, bonus program, etc. [Required] [Filter(multi eq)]

_Type_: **[CalculationMethod](Crm.DiscountTypes.md#calculationmethod)**  
Allowed values for the [CalculationMethod](Crm.DiscountTypes.md#calculationmethod) data attribute  
_Allowed Values (Crm.DiscountTypesRepository.CalculationMethod Enum Members)_  

| Value | Description |
| ---- | --- |
| StandardDiscount | StandardDiscount value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'StandardDiscount' |
| PromotionalPackage | PromotionalPackage value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'PromotionalPackage' |
| BonusProgram | BonusProgram value. Stored as 'B'. <br /> _Database Value:_ 'B' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'BonusProgram' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Code

The unique code of the DiscountType. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsSystem

Specifies whether this discount type is created and managed by the system. [Required] [Default(false)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this DiscountType. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this DiscountType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Ord

Determines the order in which the discounts are applied. The discounts with smaller Ord are applied first. [Required] [Default(1)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  



## Business Rules

[!list erp.entity=Crm.DiscountTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.DiscountTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_DiscountTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_DiscountTypes?$top=10>

