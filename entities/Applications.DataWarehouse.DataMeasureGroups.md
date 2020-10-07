# Applications.DataWarehouse.DataMeasureGroups

Contains the groups of measures in the general data warehouse. Entity: Dw_Data_Measure_Groups (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.DataWarehouse.DataMeasureGroups.md#Id) | guid |  
| [Code](Applications.DataWarehouse.DataMeasureGroups.md#Code) | string | Unique group code. [Required] [Filter(eq;like)] [ORD] 
| [Name](Applications.DataWarehouse.DataMeasureGroups.md#Name) | string | Group name (multilanguage). [Required] [Filter(eq;like)] 
| [Notes](Applications.DataWarehouse.DataMeasureGroups.md#Notes) | string (nullable) | Notes for this DataMeasureGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.DataWarehouse.DataMeasureGroups.md#Parent) | [Applications.DataWarehouse.DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md) (nullable) | Parent data measure group in the hierarchy. Null when this is root node. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Unique group code. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> Group name (multilanguage). [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this DataMeasureGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

> Parent data measure group in the hierarchy. Null when this is root node. [Filter(multi eq)]

_Type_: **[Applications.DataWarehouse.DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_DataWarehouse_DataMeasureGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_DataWarehouse_DataMeasureGroups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Dw_Data_Measure_Groups?$top=10>

