# Table Sys_Data_Sources

Contains user-defined data sources, which retrieve rows from multiple queries. Entity: Sys_Data_Sources

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Data_Source_Id|`Guid`|`PK`, Readonly||
|Base_Query_Name|`String`||The name of the query or table that is used for root reference point of the loaded data. `Required` `Filter(eq;like)` |
|Data_Source_Type|`DataSourceType`|Allowed: `M`, `D`, `S`|'M' = MULTI-TABLE (many tables); 'D' = MASTER-DETAIL (two tables); 'S' = SINGLE-TABLE . `Required` `Default("M")` `Filter(eq)` |
|Data_Source_Name|`String`||The name of the data source. `Required` `Filter(eq;like)` |
|Show_Parent_Tables|`Boolean`||Indicates whether the parent nodes in the Reference_Path in Sys_Data_Source_Queries_Table are automaticaly included in the report or not. `Required` `Default(false)` |
