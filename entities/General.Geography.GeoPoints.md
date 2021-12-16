---
uid: General.Geography.GeoPoints
---
# General.Geography.GeoPoints Entity

**Namespace:** [General.Geography](General.Geography.md)  

Geographical (geo) points are used as points of interest on the map. They are used for routing and other purposes. The points of interest for the different enterprise companies are different. Entity: Gen_Geo_Points

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Geography.GeoPoints](General.Geography.GeoPoints.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Address](General.Geography.GeoPoints.md#address) | string (128) __nullable__ | The descriptive physical address, related to this geo point. `Filter(eq;like)` 
| [Id](General.Geography.GeoPoints.md#id) | guid |  
| [Latitude](General.Geography.GeoPoints.md#latitude) | decimal (10, 7) | Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range `-90, 90`. `Required` `Default(0)` `Filter(eq;ge;le)` 
| [Longitude](General.Geography.GeoPoints.md#longitude) | decimal (10, 7) | Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range `-180, 180`. `Required` `Default(0)` `Filter(eq;ge;le)` 
| [Name](General.Geography.GeoPoints.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Geo point short name (Multilanguage). `Required` `Filter(eq;like)` 
| [RowVersion](General.Geography.GeoPoints.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](General.Geography.GeoPoints.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company for which the name of the geo point has meaning. Null for geo points not related to specific enterprise company. `Filter(multi eq)` |


## Attribute Details

### Address

The descriptive physical address, related to this geo point. `Filter(eq;like)`

_Type_: **string (128) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Latitude

Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range `-90, 90`. `Required` `Default(0)` `Filter(eq;ge;le)`

_Type_: **decimal (10, 7)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Longitude

Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range `-180, 180`. `Required` `Default(0)` `Filter(eq;ge;le)`

_Type_: **decimal (10, 7)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Name

Geo point short name (Multilanguage). `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

The enterprise company for which the name of the geo point has meaning. Null for geo points not related to specific enterprise company. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Geography.GeoPoints erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Geography.GeoPoints erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_GeoPoints?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_GeoPoints?$top=10>

