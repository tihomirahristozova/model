---
uid: Systems.Reporting.Reports
---
# Systems.Reporting.Reports Entity

**Namespace:** [Systems.Reporting](Systems.Reporting.md)  

User-defined reports. Reports retrieve data from data sources and present it in a user-defined layout. Entity: Sys_Reports

## Default Visualization
Default Display Text Format:  
_{QueryName:T}_  
Default Search Member:  
_QueryName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Reporting.Reports](Systems.Reporting.Reports.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Reporting.Reports.md#id) | guid |  
| [LayoutFormat](Systems.Reporting.Reports.md#layoutformat) | string (nullable) | Format specifier of the layout. Recognized by the application. [Filter(multi eq)] 
| [Name](Systems.Reporting.Reports.md#name) | string | Multi-language report name. [Required] [Filter(eq;like)] 
| [Notes](Systems.Reporting.Reports.md#notes) | string (nullable) | Notes for this Report. 
| [OneRow](Systems.Reporting.Reports.md#onerow) | boolean | True means that report can be used for one-row forms only. False means that the report can be used for navigators only. [Required] [Default(false)] 
| [QueryName](Systems.Reporting.Reports.md#queryname) | string | The query on which the report is based. [Required] [Filter(eq)] 
| [ReportBinaryLayout](Systems.Reporting.Reports.md#reportbinarylayout) | byte[] (nullable) | The printout layout, when the format requires binary storage. Alternative to Report_Layout. 
| [ReportLayout](Systems.Reporting.Reports.md#reportlayout) | string (nullable) | The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout. 
| [TemplateFilterXml](Systems.Reporting.Reports.md#templatefilterxml) | string (nullable) | Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. null when the current report cannot be used as template sub-report. 
| [TemplatePriority](Systems.Reporting.Reports.md#templatepriority) | int32 (nullable) | Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, null otherwise. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataSource](Systems.Reporting.Reports.md#datasource) | [DataSources](Systems.Reporting.DataSources.md) (nullable) | Report data source. If specified should be based on the query in Query_Name. null means that the report is based directly on the query. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LayoutFormat

Format specifier of the layout. Recognized by the application. [Filter(multi eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Name

Multi-language report name. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this Report.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OneRow

True means that report can be used for one-row forms only. False means that the report can be used for navigators only. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### QueryName

The query on which the report is based. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ReportBinaryLayout

The printout layout, when the format requires binary storage. Alternative to Report_Layout.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReportLayout

The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TemplateFilterXml

Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. null when the current report cannot be used as template sub-report.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TemplatePriority

Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, null otherwise.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DataSource

Report data source. If specified should be based on the query in Query_Name. null means that the report is based directly on the query. [Filter(multi eq)]

_Type_: **[DataSources](Systems.Reporting.DataSources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Reporting.Reports erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Reporting.Reports erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Reporting_Reports?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Reporting_Reports?$top=10>

