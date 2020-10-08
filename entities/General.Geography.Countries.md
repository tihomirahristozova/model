---
uid: General.Geography.Countries
---
# General.Geography.Countries

List of countries, listed by their internet suffix code. Entity: Gen_Countries

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Geography.Countries.md#Id) | guid |  
| [Code](General.Geography.Countries.md#Code) | string | Internet suffix code of the country. [Required] [Filter(eq;like)] [ORD] 
| [Name](General.Geography.Countries.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Name of the country. [Required] [Filter(like)] 
| [IntrastatCode](General.Geography.Countries.md#IntrastatCode) | string (nullable) | This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used. (Introduced in version 20.1.100.0) 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Internet suffix code of the country. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> Name of the country. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### IntrastatCode

> This code is used when creating the Intrastat Declaration. If the field is empty, then the value from the 'Code' field is used. (Introduced in version 20.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Geography.Countries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Geography.Countries erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Geography.Countries erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_Countries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_Countries?$top=10>

