---
uid: Applications.DataWarehouse.DataMeasureGroups
---
# Applications.DataWarehouse.DataMeasureGroups Entity

**Namespace:** [Applications.DataWarehouse](Applications.DataWarehouse.md)  

Contains the groups of measures in the general data warehouse. Entity: Dw_Data_Measure_Groups (Introduced in version 18.2)

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.DataWarehouse.DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.DataWarehouse.DataMeasureGroups.md#code) | string (16) | Unique group code. `Required` `Filter(eq;like)` `ORD` 
| [Id](Applications.DataWarehouse.DataMeasureGroups.md#id) | guid |  
| [Name](Applications.DataWarehouse.DataMeasureGroups.md#name) | string (254) | Group name (multilanguage). `Required` `Filter(eq;like)` 
| [Notes](Applications.DataWarehouse.DataMeasureGroups.md#notes) | string (max) __nullable__ | Notes for this DataMeasureGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.DataWarehouse.DataMeasureGroups.md#parent) | [DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md) (nullable) | Parent data measure group in the hierarchy. Null when this is root node. `Filter(multi eq)` |


## Attribute Details

### Code

Unique group code. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Group name (multilanguage). `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this DataMeasureGroup.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### Parent

Parent data measure group in the hierarchy. Null when this is root node. `Filter(multi eq)`

_Type_: **[DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_DataWarehouse_DataMeasureGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_DataWarehouse_DataMeasureGroups?$top=10>

