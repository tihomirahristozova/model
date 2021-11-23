---
uid: Systems.Reporting.Reports
---
# Systems.Reporting.Reports Entity

**Namespace:** [Systems.Reporting](Systems.Reporting.md)  

User-defined reports. Reports retrieve data from data sources and present it in a user-defined layout. Entity: Sys_Reports

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Reporting.Reports](Systems.Reporting.Reports.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Reporting.Reports.md#id) | guid |  
| [LayoutFormat](Systems.Reporting.Reports.md#layoutformat) | string (32) __nullable__ | Format specifier of the layout. Recognized by the application. `Filter(multi eq)` 
| [Name](Systems.Reporting.Reports.md#name) | string (254) | Multi-language report name. `Required` `Filter(eq;like)` 
| [Notes](Systems.Reporting.Reports.md#notes) | string (512) __nullable__ | Notes for this Report. 
| [OneRow](Systems.Reporting.Reports.md#onerow) | boolean | True means that report can be used for one-row forms only. False means that the report can be used for navigators only. `Required` `Default(false)` 
| [QueryName](Systems.Reporting.Reports.md#queryname) | string (128) | The query on which the report is based. `Required` `Filter(eq)` 
| [ReportBinaryLayout](Systems.Reporting.Reports.md#reportbinarylayout) | byte[] __nullable__ | The printout layout, when the format requires binary storage. Alternative to Report_Layout. 
| [ReportLayout](Systems.Reporting.Reports.md#reportlayout) | string (max) __nullable__ | The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout. 
| [TemplateFilterXml](Systems.Reporting.Reports.md#templatefilterxml) | string (max) __nullable__ | Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. null when the current report cannot be used as template sub-report. 
| [TemplatePriority](Systems.Reporting.Reports.md#templatepriority) | int32 __nullable__ | Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, null otherwise. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataSource](Systems.Reporting.Reports.md#datasource) | [DataSources](Systems.Reporting.DataSources.md) (nullable) | Report data source. If specified should be based on the query in Query_Name. null means that the report is based directly on the query. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LayoutFormat

Format specifier of the layout. Recognized by the application. `Filter(multi eq)`

_Type_: **string (32) __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### Name

Multi-language report name. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this Report.

_Type_: **string (512) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **512**  

### OneRow

True means that report can be used for one-row forms only. False means that the report can be used for navigators only. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### QueryName

The query on which the report is based. `Required` `Filter(eq)`

_Type_: **string (128)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### ReportBinaryLayout

The printout layout, when the format requires binary storage. Alternative to Report_Layout.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReportLayout

The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### TemplateFilterXml

Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. null when the current report cannot be used as template sub-report.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### TemplatePriority

Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, null otherwise.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DataSource

Report data source. If specified should be based on the query in Query_Name. null means that the report is based directly on the query. `Filter(multi eq)`

_Type_: **[DataSources](Systems.Reporting.DataSources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Reporting.Reports erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Reporting.Reports erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Reporting_Reports?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Reporting_Reports?$top=10>

