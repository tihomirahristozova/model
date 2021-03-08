# Table Rent_Assets

Contains the rentable assets. Entity: Rent_Assets

# Aggregate Hierarchy

* [Rent_Asset_Groups](Rent_Asset_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Rental_Asset_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||True if the asset is currently active and may be used in new documents. Deactivated assets are used only in reports. `Required` `Default(true)` `Filter(eq)` |
|Notes|`String`||Notes for this Asset. |
|Rental_Asset_Code|`String`||Unique rental asset code. `Required` `Filter(eq;like)` `ORD` |
|Rental_Asset_Name|`String`||The name of the rental asset. `Required` `Filter(like)` |
|Time_Period_Type|`TimePeriodType?`|Allowed: `D`, `M`|Specifies the unit by which the periods of renting of this asset are measured. Possible values are: 'by days' or 'by months'. `Filter(multi eq)` |
