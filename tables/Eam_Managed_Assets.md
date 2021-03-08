# Table Eam_Managed_Assets

Contains the managed assets. The management of assets include maintenance planning and execution, location assignments tracking, etc. Entity: Eam_Managed_Assets (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Managed_Asset_Id|`Guid`|`PK`, Readonly||
|Managed_Asset_Code|`String`||Unique code of the managed asset. The code is unique among all managed assets in the same enterprise company. `Required` `Filter(eq;like)` |
|Managed_Asset_Name|`MultilanguageString`||Name of the managed asset (multi-language). `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this ManagedAsset. |
|Registration_Number|`String`||Registration number of the asset with the national registration authorities. null means the registation number is unknown or N/A. `Filter(eq;like)` |
