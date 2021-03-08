# Table Gen_Product_Group_Range_Properties

When specified for a product group, provides a way for automatical creation of new products, based on altering a set of values of some user-defined properties. Each value combination is used to create a new, unique product within the group. Entity: Gen_Product_Group_Range_Properties

# Aggregate Hierarchy

* [Gen_Product_Groups](Gen_Product_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Range_Property_Id|`Guid`|`PK`, Readonly||
|From_Property_Value|`String`||Starting value of the range of alternative values. Used only when Rage Type = R (range). |
|Property_Values_List|`String`||Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio). |
|Range_Type|`RangeType`|Allowed: `R`, `L`|Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;. `Required` `Default("R")` |
|To_Property_Value|`String`||Ending value of the range of alternative values. Used only when Rage Type = R (range). |
