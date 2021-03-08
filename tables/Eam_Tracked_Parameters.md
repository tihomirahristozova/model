# Table Eam_Tracked_Parameters

Parameters of assets, tracked for maintenance reasons, like car mileage, aircraft cycles, etc. Entity: Eam_Tracked_Parameters (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Tracked_Parameter_Id|`Guid`|`PK`, Readonly||
|Tracked_Parameter_Code|`String`||Unique code of the asset parameter. `Required` `Filter(multi eq;like)` `ORD` |
|Is_Active|`Boolean`||Specifies whether the parameter is active for choosing in drop downs. `Required` `Default(true)` `Filter(multi eq)` |
|Tracked_Parameter_Name|`MultilanguageString`||Multilanguage name of the asset parameter. `Required` `Filter(multi eq;like)` |
|Notes|`String`||Notes for this TrackedParameter. `Filter(like)` |
