---
uid: General.ReportQueries
---
# General.ReportQueries

Contains the sub-queries, which a report contains. Entity: Gen_Report_Queries

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.ReportQueries.md#Id) | guid |  
| [DependsOnChildRows](General.ReportQueries.md#DependsOnChildRows) | boolean | If True the data in the current report table contains only the rows that have child rows in sub-tables. [Required] [Default(false)] 
| [ExtensionsList](General.ReportQueries.md#ExtensionsList) | string (nullable) | A comma separated list of report extension names. An extension is set of additional fields that participate in the query. 
| [FilterXml](General.ReportQueries.md#FilterXml) | dataaccessfilter (nullable) | Filter for the loaded table. 
| [ReferencePath](General.ReportQueries.md#ReferencePath) | string | A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. [Required] 
| [ShowCustomProperties](General.ReportQueries.md#ShowCustomProperties) | boolean | True to include the custom properties. [Required] [Default(false)] 
| [ShowTextColumns](General.ReportQueries.md#ShowTextColumns) | boolean | True to include text descriptions for certain columns. [Required] [Default(false)] 
| [TableName](General.ReportQueries.md#TableName) | string (nullable) | The name of the report query. A Reference_Path can participate more than one time in the report but with different Report_Query_Name. This can be used to specify different filter for the same query. Can be null. 
| [UniqueName](General.ReportQueries.md#UniqueName) | string (nullable) | The name of the data table in the printout datasource. If null the Reference_Path is used. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Report](General.ReportQueries.md#Report) | [General.Reports](General.Reports.md) | The [Report](General.ReportQueries.md#Report) to which this ReportQuery belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DependsOnChildRows

> If True the data in the current report table contains only the rows that have child rows in sub-tables. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

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

### ReferencePath

> A sequence of table names and foreign key columns that define how the data will be loaded by this query. For example - Gen_Documents/Enterprise_Company_Id/Company_Id - will load the definition of the company for the enterprise company of a document. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ShowCustomProperties

> True to include the custom properties. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ShowTextColumns

> True to include text descriptions for certain columns. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

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

### Report

> The [Report](General.ReportQueries.md#Report) to which this ReportQuery belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Reports](General.Reports.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.ReportQueries erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.ReportQueries erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.ReportQueries erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_ReportQueries?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_ReportQueries?$top=10>

