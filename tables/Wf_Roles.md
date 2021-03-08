# Table Wf_Roles

The various roles, which the users can play. Entity: Wf_Roles

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Role_Id|`Guid`|`PK`, Readonly||
|Role_Name|`String`||The name of this Role. `Required` `Filter(eq;like)` `ORD` |
|Role_Description|`String`||Description of the role. |
|Visual_Style|`String`||The default visual style for the user interface. |
