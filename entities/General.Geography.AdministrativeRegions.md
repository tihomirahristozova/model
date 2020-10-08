---
uid: General.Geography.AdministrativeRegions
---
# General.Geography.AdministrativeRegions

Hierarchical structure of the legally defined administrative regions. Administrative regions are sub-divisions of the countries. Entity: Gen_Administrative_Regions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Geography.AdministrativeRegions.md#Id) | guid |  
| [Code](General.Geography.AdministrativeRegions.md#Code) | string | Administrative code of country territorial subdivision. [Required] [Filter(eq;like)] 
| [Name](General.Geography.AdministrativeRegions.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Name of country territorial subdivision. [Required] [Filter(like)] 
| [FullPath](General.Geography.AdministrativeRegions.md#FullPath) | string (nullable) | Full identification path of the current country territorial subdivision. [Filter(eq;like)] 
| [ParentFullPath](General.Geography.AdministrativeRegions.md#ParentFullPath) | string (nullable) | Parent region of the current territorial subdivision. [Filter(eq;like)] 
| [ValidFrom](General.Geography.AdministrativeRegions.md#ValidFrom) | date (nullable) | Start date of validity of this administrative division. null when the starting date is unknown in the past. [Filter(ge;le)] 
| [ValidTo](General.Geography.AdministrativeRegions.md#ValidTo) | date (nullable) | End date of validity of this administative division. null when the division is still active or ending date is unknown. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Country](General.Geography.AdministrativeRegions.md#Country) | [General.Geography.Countries](General.Geography.Countries.md) | Country of the territorial subdivision. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Administrative code of country territorial subdivision. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Name of country territorial subdivision. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### FullPath

> Full identification path of the current country territorial subdivision. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ParentFullPath

> Parent region of the current territorial subdivision. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ValidFrom

> Start date of validity of this administrative division. null when the starting date is unknown in the past. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ValidTo

> End date of validity of this administative division. null when the division is still active or ending date is unknown. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Country

> Country of the territorial subdivision. [Required] [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Geography.AdministrativeRegions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Geography.AdministrativeRegions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Geography.AdministrativeRegions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_AdministrativeRegions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_AdministrativeRegions?$top=10>

