---
uid: Systems.Reporting.DataSourceQueries
---
# Systems.Reporting.DataSourceQueries Entity

**Namespace:** [Systems.Reporting](Systems.Reporting.md)  

Represents a query within a data source. Entity: Sys_Data_Source_Queries

## Default Visualization
Default Display Text Format:  
_{TableName}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Reporting.DataSources](Systems.Reporting.DataSources.md)  
Aggregate Root:  
[Systems.Reporting.DataSources](Systems.Reporting.DataSources.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DependsOnChildRows](Systems.Reporting.DataSourceQueries.md#dependsonchildrows) | [DependsOnChildRows](Systems.Reporting.DataSourceQueries.md#dependsonchildrows) | Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows. `Required` `Default(0)` 
| [ExtensionsList](Systems.Reporting.DataSourceQueries.md#extensionslist) | string (max) __nullable__ | A comma separated list of report extension names. An extension is set of additional fields that participate in the query. 
| [FilterXml](Systems.Reporting.DataSourceQueries.md#filterxml) | dataaccessfilter __nullable__ | Filter for the loaded table. 
| [FirstRow](Systems.Reporting.DataSourceQueries.md#firstrow) | boolean | Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable. `Required` `Default(false)` 
| [Id](Systems.Reporting.DataSourceQueries.md#id) | guid |  
| [ReferencePath](Systems.Reporting.DataSourceQueries.md#referencepath) | string (max) | A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/<br />Enterprise_Company_<br />Id/Company_Id - will load the definition of the company for the enterprise company of a document. `Required` 
| [TableName](Systems.Reporting.DataSourceQueries.md#tablename) | string (64) __nullable__ | The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null. 
| [UniqueName](Systems.Reporting.DataSourceQueries.md#uniquename) | string (64) __nullable__ | The name of the data table in the printout datasource. If null the Reference_Path is used. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataSource](Systems.Reporting.DataSourceQueries.md#datasource) | [DataSources](Systems.Reporting.DataSources.md) | The report of the query. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DependsOnChildRows

Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows. `Required` `Default(0)`

_Type_: **[DependsOnChildRows](Systems.Reporting.DataSourceQueries.md#dependsonchildrows)**  
Allowed values for the `DependsOnChildRows`(Systems.Reporting.DataSourceQueries.md#dependsonchildrows) data attribute  
_Allowed Values (Systems.Reporting.DataSourceQueriesRepository.DependsOnChildRows Enum Members)_  

| Value | Description |
| ---- | --- |
| NoChildRowDependency | NoChildRowDependency value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoChildRowDependency' |
| TheRowIsVisible<br />IfThereIsAtLeast<br />OneChildRow | TheRowIsVisible<br />IfThereIsAtLeast<br />OneChildRow value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'TheRowIsVisible<br />IfThereIsAtLeast<br />OneChildRow' |
| TheRowIsVisible<br />IfAllSubTables<br />ContainChildRows | TheRowIsVisible<br />IfAllSubTables<br />ContainChildRows value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'TheRowIsVisible<br />IfAllSubTables<br />ContainChildRows' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

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

### FirstRow

Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ReferencePath

A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. `Required`

_Type_: **string (max)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

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

### DataSource

The report of the query. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DataSources](Systems.Reporting.DataSources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Reporting.DataSourceQueries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Reporting.DataSourceQueries erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Reporting_DataSourceQueries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Reporting_DataSourceQueries?$top=10>

