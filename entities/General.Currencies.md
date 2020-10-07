# General.Currencies

List of user-defined currencies. Entity: Gen_Currencies

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Currencies.md#Id) | guid |  
| [Name](General.Currencies.md#Name) | string | The name of this Currency. [Required] [Filter(like)] 
| [CurrencySign](General.Currencies.md#CurrencySign) | string | The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'. [Required] [Filter(eq;like)] [ORD] 
| [ShowOrder](General.Currencies.md#ShowOrder) | int32 | The order in which to show the currency in combo boxes, etc. [Required] [Default(0)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> The name of this Currency. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CurrencySign

> The international currency designator, as defined in ISO 4217. For example euro is represented as 'EUR'. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ShowOrder

> The order in which to show the currency in combo boxes, etc. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  



## Business Rules

[!list erp.entity=General.Currencies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Currencies erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Currencies erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Currencies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Currencies?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Currencies?$top=10>

