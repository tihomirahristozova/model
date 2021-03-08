# Table Sec_Visual_Permissions

Contains permissions, which are honored only by client applications and are used to provide access to (primarily show/hide) different elements of the user interface. Entity: Sec_Visual_Permissions

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Visual_Permission_Id|`Guid`|`PK`, Readonly||
|Application_Name|`String`||The application for which the permission is specified. `Required` `Filter(eq)` |
|Element_Name|`String`||Optionally, the element from the panel which will be secured. `Filter(eq)` |
|Form_Name|`String`||Optionally, the form which will be secured. `Filter(eq)` |
|Operation_Name|`String`||Optionally, the operation on the element which will be secured. `Filter(eq)` |
|Panel_Name|`String`||Optionally, the panel from the form which will be secured. `Filter(eq)` |
