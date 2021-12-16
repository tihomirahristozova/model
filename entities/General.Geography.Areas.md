---
uid: General.Geography.Areas
---
# General.Geography.Areas Entity

**Namespace:** [General.Geography](General.Geography.md)  

Areas are user-defined division of the sales territories. Entity: Gen_Areas

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Geography.Areas](General.Geography.Areas.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Geography.Areas.md#code) | string (16) | The unique code of the Area. `Required` `Filter(eq;like)` `ORD` 
| [FullPath](General.Geography.Areas.md#fullpath) | string (254) __nullable__ | Full path to the area, starting with '/' and containing the area codes of all parent areas using '/' as separator and terminator. For example root area with code 'BG' would have full path = '/BG/'. `Filter(eq;like)` `ReadOnly` 
| [Id](General.Geography.Areas.md#id) | guid |  
| [Name](General.Geography.Areas.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Obsolete. Not used. `Required` `Filter(eq;like)` `ORD` 
| [RowVersion](General.Geography.Areas.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](General.Geography.Areas.md#parent) | [Areas](General.Geography.Areas.md) (nullable) | Parent area in the hierarchy. `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the Area. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### FullPath

Full path to the area, starting with '/' and containing the area codes of all parent areas using '/' as separator and terminator. For example root area with code 'BG' would have full path = '/BG/'. `Filter(eq;like)` `ReadOnly`

_Type_: **string (254) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Obsolete. Not used. `Required` `Filter(eq;like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

Parent area in the hierarchy. `Filter(multi eq)`

_Type_: **[Areas](General.Geography.Areas.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Geography.Areas erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Geography.Areas erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Geography_Areas?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Geography_Areas?$top=10>

