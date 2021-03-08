# Table Inv_Store_Bins

The storage locations within a store. If there are no differentiated storage locations, create only one, called “(Default)” or similar. Entity: Inv_Store_Bins

# Aggregate Hierarchy

* [Inv_Stores](Inv_Stores.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Is_Default|`Boolean`||True, when this is the default storage bin for the specified store. `Required` `Default(false)` |
|Store_Bin_Name|`String`||Name of the store bin. `Required` `Filter(like)` |
