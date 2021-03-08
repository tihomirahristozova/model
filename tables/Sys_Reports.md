# Table Sys_Reports

User-defined reports. Reports retrieve data from data sources and present it in a user-defined layout. Entity: Sys_Reports

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Report_Id|`Guid`|`PK`, Readonly||
|Layout_Format|`String`||Format specifier of the layout. Recognized by the application. `Filter(multi eq)` |
|Report_Name|`String`||Multi-language report name. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this Report. |
|One_Row|`Boolean`||True means that report can be used for one-row forms only. False means that the report can be used for navigators only. `Required` `Default(false)` |
|Query_Name|`String`||The query on which the report is based. `Required` `Filter(eq)` |
|Report_Binary_Layout|`Byte[]`|`BLOB`|The printout layout, when the format requires binary storage. Alternative to Report_Layout. |
|Report_Layout|`String`||The textual representation of the printout layout, when the format requires text representation. Alternative to Report_Binary_Layout. |
|Template_Filter_Xml|`String`||Specifies the filter condition, which must be satisfied in order for this report to be prioritized for printing as a template sub-report. null when the current report cannot be used as template sub-report. |
|Template_Priority|`Int32?`||Specifies the priority of the current report, relative to other reports. Used only when choosing which report to show as a template subreport, null otherwise. |
