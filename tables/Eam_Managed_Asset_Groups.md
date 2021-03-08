# Table Eam_Managed_Asset_Groups

Organizational hierarchy of asset groups. Entity: Eam_Managed_Asset_Groups (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Managed_Asset_Group_Id|`Guid`|`PK`, Readonly||
|Managed_Asset_Group_Code|`String`||Unique (within all groups) code of the asset group. `Required` `Filter(multi eq;like)` `ORD` |
|Managed_Asset_Group_Name|`MultilanguageString`||Name of the asset group (multi-language). `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this ManagedAssetGroup. |
