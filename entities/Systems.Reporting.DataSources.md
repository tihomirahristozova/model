---
uid: Systems.Reporting.DataSources
---
# Systems.Reporting.DataSources

Contains user-defined data sources, which retrieve rows from multiple queries. Entity: Sys_Data_Sources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Reporting.DataSources.md#Id) | guid |  
| [BaseQueryName](Systems.Reporting.DataSources.md#BaseQueryName) | string | The name of the query or table that is used for root reference point of the loaded data. [Required] [Filter(eq;like)] 
| [Name](Systems.Reporting.DataSources.md#Name) | string | The name of the data source. [Required] [Filter(eq;like)] 
| [DataSourceType](Systems.Reporting.DataSources.md#DataSourceType) | [Systems.Reporting.DataSourcesRepository.DataSourceType](Systems.Reporting.DataSources.md#DataSourceType) | 'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE . [Required] [Default("M")] [Filter(eq)] 
| [ShowParentTables](Systems.Reporting.DataSources.md#ShowParentTables) | boolean | Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not. [Required] [Default(false)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Queries | [Systems.Reporting.DataSourceQueries](Systems.Reporting.DataSourceQueries.md) | List of [DataSourceQuery](Systems.Reporting.DataSourceQueries.md) child objects, based on the [Systems.Reporting.DataSourceQuery.DataSource](Systems.Reporting.DataSourceQueries.md#DataSource) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BaseQueryName

> The name of the query or table that is used for root reference point of the loaded data. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Name

> The name of the data source. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### DataSourceType

> 'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE . [Required] [Default("M")] [Filter(eq)]

_Type_: **[Systems.Reporting.DataSourcesRepository.DataSourceType](Systems.Reporting.DataSources.md#DataSourceType)**  
Allowed values for the [DataSourceType](Systems.Reporting.DataSources.md#DataSourceType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| MultiTable | MultiTable value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'MultiTable' |
| MasterDetail | MasterDetail value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'MasterDetail' |
| SingleTable | SingleTable value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'SingleTable' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **MultiTable**  

### ShowParentTables

> Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  



## Business Rules

[!list erp.entity=Systems.Reporting.DataSources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Reporting.DataSources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Reporting.DataSources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Reporting_DataSources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Reporting_DataSources?$top=10>

