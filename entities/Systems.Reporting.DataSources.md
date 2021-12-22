---
uid: Systems.Reporting.DataSources
---
# Systems.Reporting.DataSources Entity

**Namespace:** [Systems.Reporting](Systems.Reporting.md)  

Contains user-defined data sources, which retrieve rows from multiple queries. Entity: Sys_Data_Sources

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Reporting.DataSources](Systems.Reporting.DataSources.md)  
  * [Systems.Reporting.DataSourceQueries](Systems.Reporting.DataSourceQueries.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseQueryName](Systems.Reporting.DataSources.md#basequeryname) | string (128) | The name of the query or table that is used for root reference point of the loaded data. `Required` `Filter(eq;like)` 
| [DataSourceType](Systems.Reporting.DataSources.md#datasourcetype) | [DataSourceType](Systems.Reporting.DataSources.md#datasourcetype) | 'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE . `Required` `Default("M")` `Filter(eq)` 
| [Id](Systems.Reporting.DataSources.md#id) | guid |  
| [Name](Systems.Reporting.DataSources.md#name) | string (64) | The name of the data source. `Required` `Filter(eq;like)` 
| [ObjectVersion](Systems.Reporting.DataSources.md#objectversion) | int32 |  
| [ShowParentTables](Systems.Reporting.DataSources.md#showparenttables) | boolean | Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_<br />Queries_Table are automaticaly included in the report or not. `Required` `Default(false)` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Queries | [DataSourceQueries](Systems.Reporting.DataSourceQueries.md) | List of `DataSourceQuery`(Systems.Reporting.DataSourceQueries.md) child objects, based on the `Systems.Reporting.DataSourceQuery.DataSource`(Systems.Reporting.DataSourceQueries.md#datasource) back reference 


## Attribute Details

### BaseQueryName

The name of the query or table that is used for root reference point of the loaded data. `Required` `Filter(eq;like)`

_Type_: **string (128)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### DataSourceType

'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE . `Required` `Default("M")` `Filter(eq)`

_Type_: **[DataSourceType](Systems.Reporting.DataSources.md#datasourcetype)**  
Allowed values for the `DataSourceType`(Systems.Reporting.DataSources.md#datasourcetype) data attribute  
_Allowed Values (Systems.Reporting.DataSourcesRepository.DataSourceType Enum Members)_  

| Value | Description |
| ---- | --- |
| MultiTable | MultiTable value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'MultiTable' |
| MasterDetail | MasterDetail value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'MasterDetail' |
| SingleTable | SingleTable value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'SingleTable' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **MultiTable**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of the data source. `Required` `Filter(eq;like)`

_Type_: **string (64)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ShowParentTables

Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Reporting.DataSources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Reporting.DataSources erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Reporting_DataSources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Reporting_DataSources?$top=10>

