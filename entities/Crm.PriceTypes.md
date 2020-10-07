# Crm.PriceTypes

Price types. Entity: Crm_Price_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.PriceTypes.md#Id) | guid |  
| [Notes](Crm.PriceTypes.md#Notes) | string (nullable) | Notes for this PriceType. 
| [OrdinalPos](Crm.PriceTypes.md#OrdinalPos) | int32 | Priority position of the price type, with respect to the other price types. [Required] [ORD] 
| [Code](Crm.PriceTypes.md#Code) | string | Short identification code of the price type. [Required] [Filter(eq)] [ORD] 
| [Name](Crm.PriceTypes.md#Name) | string | Full name of the price type. [Required] [Filter(eq;like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

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

### Code

> Short identification code of the price type. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Name

> Full name of the price type. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



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

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Price_Types?$top=10>

