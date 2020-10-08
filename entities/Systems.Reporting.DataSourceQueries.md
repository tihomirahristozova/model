---
uid: Systems.Reporting.DataSourceQueries
---
# Systems.Reporting.DataSourceQueries

Represents a query within a data source. Entity: Sys_Data_Source_Queries

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DependsOnChildRows](Systems.Reporting.DataSourceQueries.md#dependsonchildrows) | [DependsOnChildRows](Systems.Reporting.DataSourceQueries.md#dependsonchildrows) | Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows. [Required] [Default(0)] 
| [ExtensionsList](Systems.Reporting.DataSourceQueries.md#extensionslist) | string (nullable) | A comma separated list of report extension names. An extension is set of additional fields that participate in the query. 
| [FilterXml](Systems.Reporting.DataSourceQueries.md#filterxml) | dataaccessfilter (nullable) | Filter for the loaded table. 
| [FirstRow](Systems.Reporting.DataSourceQueries.md#firstrow) | boolean | Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable. [Required] [Default(false)] 
| [Id](Systems.Reporting.DataSourceQueries.md#id) | guid |  
| [ReferencePath](Systems.Reporting.DataSourceQueries.md#referencepath) | string | A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. [Required] 
| [TableName](Systems.Reporting.DataSourceQueries.md#tablename) | string (nullable) | The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null. 
| [UniqueName](Systems.Reporting.DataSourceQueries.md#uniquename) | string (nullable) | The name of the data table in the printout datasource. If null the Reference_Path is used. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataSource](Systems.Reporting.DataSourceQueries.md#datasource) | [Systems.Reporting.DataSources](Systems.Reporting.DataSources.md) | The report of the query. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### DependsOnChildRows

> Determines the visibility of rows in this table. 0 - allways visible; 1 - the row is visible if there is at least one child row; 2 - the row is visible if all sub-tables contain child rows. [Required] [Default(0)]

_Type_: **[DependsOnChildRows](Systems.Reporting.DataSourceQueries.md#dependsonchildrows)**  
Allowed values for the [DependsOnChildRows](Systems.Reporting.DataSourceQueries.md#dependsonchildrows) data attribute  
_Allowed Values (Systems.Reporting.DataSourceQueriesRepository.DependsOnChildRows Enum Members)_  

| Value | Description |
| ---- | --- |
| NoChildRowDependency | NoChildRowDependency value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NoChildRowDependency' |
| TheRowIsVisibleIfThereIsAtLeastOneChildRow | TheRowIsVisibleIfThereIsAtLeastOneChildRow value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'TheRowIsVisibleIfThereIsAtLeastOneChildRow' |
| TheRowIsVisibleIfAllSubTablesContainChildRows | TheRowIsVisibleIfAllSubTablesContainChildRows value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'TheRowIsVisibleIfAllSubTablesContainChildRows' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ExtensionsList

> A comma separated list of report extension names. An extension is set of additional fields that participate in the query.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FilterXml

> Filter for the loaded table.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FirstRow

> Specifies, that only the first row of the current query will be retrieved. Used and applied only when the data source type is not multitable. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ReferencePath

> A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TableName

> The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UniqueName

> The name of the data table in the printout datasource. If null the Reference_Path is used.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DataSource

> The report of the query. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Reporting.DataSources](Systems.Reporting.DataSources.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Reporting.DataSourceQueries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Reporting.DataSourceQueries erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Reporting.DataSourceQueries erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Reporting_DataSourceQueries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Reporting_DataSourceQueries?$top=10>

