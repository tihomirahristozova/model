# Table Sec_Column_Permissions

User permissions for accessing the system data columns. Entity: Sec_Column_Permissions

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Column_Permission_Id|`Guid`|`PK`, Readonly||
|Column_Name|`String`||The name of the secured column. `Required` `Filter(eq)` |
|Table_Name|`String`||The table in which is the secured column. `Required` `Filter(eq)` `ORD` |
