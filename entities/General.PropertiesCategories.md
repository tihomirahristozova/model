# General.PropertiesCategories

Categories of properties. Entity: Gen_Properties_Categories

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.PropertiesCategories.md#Id) | guid |  
| [Name](General.PropertiesCategories.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this PropertiesCategory. [Required] [Filter(eq;like)] [ORD] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> The name of this PropertiesCategory. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=General.PropertiesCategories erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.PropertiesCategories erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.PropertiesCategories erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PropertiesCategories?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PropertiesCategories?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Properties_Categories?$top=10>

