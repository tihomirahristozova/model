---
uid: Crm.PriceTypes
---
# Crm.PriceTypes

Price types. Entity: Crm_Price_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Crm.PriceTypes.md#code) | string | Short identification code of the price type. [Required] [Filter(eq)] [ORD] 
| [Id](Crm.PriceTypes.md#id) | guid |  
| [Name](Crm.PriceTypes.md#name) | string | Full name of the price type. [Required] [Filter(eq;like)] 
| [Notes](Crm.PriceTypes.md#notes) | string (nullable) | Notes for this PriceType. 
| [OrdinalPos](Crm.PriceTypes.md#ordinalpos) | int32 | Priority position of the price type, with respect to the other price types. [Required] [ORD] 


## Attribute Details

### Code

> Short identification code of the price type. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Full name of the price type. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this PriceType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrdinalPos

> Priority position of the price type, with respect to the other price types. [Required] [ORD]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=Crm.PriceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.PriceTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.PriceTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PriceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PriceTypes?$top=10>

