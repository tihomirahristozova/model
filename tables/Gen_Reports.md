# Table Gen_Reports

Contains user-defined data-sources. The data sources is a user-defined way (similar to query designer) to extract, filter, join and transform data for presentation purposes. Entity: Gen_Reports

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Report_Id|`Guid`|`PK`, Readonly||
|Is_Table|`Boolean`||If True the Query_Name is name of a table, otherwise is name of a query that can be filtered with Filter_Xml. . `Required` `Default(true)` `Filter(eq)` |
|Report_Name|`String`||The name of this Report. `Required` `Filter(eq;like)` |
|Query_Name|`String`||The name of the query or table that is used for root reference point of the loaded data. `Required` `Filter(eq;like)` |
|Show_Parent_Tables|`Boolean`||Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not. `Required` `Default(false)` |
