# Table Eam_Managed_Asset_Types

Types of managed assets. Used to categorize the assets and the tracked parameters for each type. Entity: Eam_Managed_Asset_Types (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Managed_Asset_Type_Id|`Guid`|`PK`, Readonly||
|Managed_Asset_Type_Code|`String`||Unique code of the asset type. `Required` `Filter(multi eq;like)` `ORD` |
|Is_Active|`Boolean`||Specifies whether the asset type is active for choosing in drop-down choices. `Required` `Default(true)` |
|Managed_Asset_Type_Name|`MultilanguageString`||Multilanguage name of the asset type. `Required` `Filter(multi eq;like)` |
|Notes|`String`||Notes for this ManagedAssetType. |
