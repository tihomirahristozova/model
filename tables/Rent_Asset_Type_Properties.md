# Table Rent_Asset_Type_Properties

Contains the properties, which are required for each asset category. Entity: Rent_Asset_Type_Properties

# Aggregate Hierarchy

* [Rent_Asset_Types](Rent_Asset_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Rental_Asset_Type_Property_Id|`Guid`|`PK`, Readonly||
|Default_Value|`String`||The default value of the property. `Filter(like)` |
|Default_Value_Id|`Guid?`||The value id of the default value of the property. `Filter(multi eq)` |
