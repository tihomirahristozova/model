# Table Eam_Managed_Asset_Locations

Contains the locations to which the assets are assigned at various moments in time. Entity: Eam_Managed_Asset_Locations (Introduced in version 19.1)

# Aggregate Hierarchy

* [Eam_Managed_Assets](Eam_Managed_Assets.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Managed_Asset_Location_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime`||The date on which the asset is assigned to the location. `Required` `Default(Now)` |
|Notes|`String`||Might contain additional notes for the exact location of the asset within the enterprise company location. |
