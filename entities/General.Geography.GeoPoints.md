---
uid: General.Geography.GeoPoints
---
# General.Geography.GeoPoints

Geographical (geo) points are used as points of interest on the map. They are used for routing and other purposes. The points of interest for the different enterprise companies are different. Entity: Gen_Geo_Points

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Geography.GeoPoints.md#Id) | guid |  
| [Address](General.Geography.GeoPoints.md#Address) | string (nullable) | The descriptive physical address, related to this geo point. [Filter(eq;like)] 
| [Name](General.Geography.GeoPoints.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Geo point short name (Multilanguage). [Required] [Filter(eq;like)] 
| [Latitude](General.Geography.GeoPoints.md#Latitude) | decimal | Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90]. [Required] [Default(0)] [Filter(eq;ge;le)] 
| [Longitude](General.Geography.GeoPoints.md#Longitude) | decimal | Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180]. [Required] [Default(0)] [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](General.Geography.GeoPoints.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company for which the name of the geo point has meaning. Null for geo points not related to specific enterprise company. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Address

> The descriptive physical address, related to this geo point. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> Geo point short name (Multilanguage). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Latitude

> Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90]. [Required] [Default(0)] [Filter(eq;ge;le)]

_Type_: **decimal**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Longitude

> Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180]. [Required] [Default(0)] [Filter(eq;ge;le)]

_Type_: **decimal**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### EnterpriseCompany

> The enterprise company for which the name of the geo point has meaning. Null for geo points not related to specific enterprise company. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Geography.GeoPoints erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Geography.GeoPoints erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Geography.GeoPoints erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_GeoPoints?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_GeoPoints?$top=10>

