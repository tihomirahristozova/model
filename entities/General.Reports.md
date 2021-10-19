---
uid: General.Reports
---
# General.Reports Entity

**Namespace:** [General](General.md)  

Contains user-defined data-sources. The data sources is a user-defined way (similar to query designer) to extract, filter, join and transform data for presentation purposes. Entity: Gen_Reports

## Default Visualization
Default Display Text Format:  
_{QueryName}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Reports](General.Reports.md)  
  * [General.ReportQueries](General.ReportQueries.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Reports.md#id) | guid |  
| [IsTable](General.Reports.md#istable) | boolean | If True the Query_Name is name of a table, otherwise is name of a query that can be filtered with Filter_Xml. . `Required` `Default(true)` `Filter(eq)` 
| [Name](General.Reports.md#name) | string (64) | The name of this Report. `Required` `Filter(eq;like)` 
| [QueryName](General.Reports.md#queryname) | string (128) | The name of the query or table that is used for root reference point of the loaded data. `Required` `Filter(eq;like)` 
| [ShowParentTables](General.Reports.md#showparenttables) | boolean | Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_<br />Queries_Table are automaticaly included in the report or not. `Required` `Default(false)` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Queries | [ReportQueries](General.ReportQueries.md) | List of `ReportQuery`(General.ReportQueries.md) child objects, based on the `General.ReportQuery.Report`(General.ReportQueries.md#report) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsTable

If True the Query_Name is name of a table, otherwise is name of a query that can be filtered with Filter_Xml. . `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of this Report. `Required` `Filter(eq;like)`

_Type_: **string (64)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### QueryName

The name of the query or table that is used for root reference point of the loaded data. `Required` `Filter(eq;like)`

_Type_: **string (128)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### ShowParentTables

Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  



## Business Rules

[!list limit=1000 erp.entity=General.Reports erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Reports erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Reports?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Reports?$top=10>

