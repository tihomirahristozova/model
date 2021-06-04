---
uid: General.ReportQueries
---
# General.ReportQueries Entity

**Namespace:** [General](General.md)  

Contains the sub-queries, which a report contains. Entity: Gen_Report_Queries

## Default Visualization
Default Display Text Format:  
_{TableName:T}_  
Default Search Member:  
_TableName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Reports](General.Reports.md)  
Aggregate Root:  
[General.Reports](General.Reports.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DependsOnChildRows](General.ReportQueries.md#dependsonchildrows) | boolean | If True the data in the current report table contains only the rows that have child rows in sub-tables. `Required` `Default(false)` 
| [ExtensionsList](General.ReportQueries.md#extensionslist) | string (max) __nullable__ | A comma separated list of report extension names. An extension is set of additional fields that participate in the query. 
| [FilterXml](General.ReportQueries.md#filterxml) | dataaccessfilter __nullable__ | Filter for the loaded table. 
| [Id](General.ReportQueries.md#id) | guid |  
| [ReferencePath](General.ReportQueries.md#referencepath) | string (512) | A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/<br />Enterprise_Company_<br />Id/Company_Id - will load the definition of the company for the enterprise company of a document. `Required` 
| [ShowCustomProperties](General.ReportQueries.md#showcustomproperties) | boolean | True to include the custom properties. `Required` `Default(false)` 
| [ShowTextColumns](General.ReportQueries.md#showtextcolumns) | boolean | True to include text descriptions for certain columns. `Required` `Default(false)` 
| [TableName](General.ReportQueries.md#tablename) | string (64) __nullable__ | The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null. 
| [UniqueName](General.ReportQueries.md#uniquename) | string (64) __nullable__ | The name of the data table in the printout datasource. If null the Reference_Path is used. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Report](General.ReportQueries.md#report) | [Reports](General.Reports.md) | The `Report`(General.ReportQueries.md#report) to which this ReportQuery belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DependsOnChildRows

If True the data in the current report table contains only the rows that have child rows in sub-tables. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ExtensionsList

A comma separated list of report extension names. An extension is set of additional fields that participate in the query.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### FilterXml

Filter for the loaded table.

_Type_: **dataaccessfilter __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ReferencePath

A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. `Required`

_Type_: **string (512)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **512**  

### ShowCustomProperties

True to include the custom properties. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ShowTextColumns

True to include text descriptions for certain columns. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### TableName

The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null.

_Type_: **string (64) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### UniqueName

The name of the data table in the printout datasource. If null the Reference_Path is used.

_Type_: **string (64) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


## Reference Details

### Report

The `Report`(General.ReportQueries.md#report) to which this ReportQuery belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Reports](General.Reports.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  



## Business Rules

[!list erp.entity=General.ReportQueries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.ReportQueries erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_ReportQueries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_ReportQueries?$top=10>

