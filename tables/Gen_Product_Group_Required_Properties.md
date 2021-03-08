# Table Gen_Product_Group_Required_Properties

Contains the properties, that are required to be set, when creating new products in the category and its sub-categories. Entity: Gen_Product_Group_Required_Properties

# Aggregate Hierarchy

* [Gen_Product_Groups](Gen_Product_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Required_Property_Id|`Guid`|`PK`, Readonly||
|Default_Property_Value|`String`||When not null, specifies the default value of the property, for new products in the group. |
|Default_Property_Value_Description|`String`||When not null, specifies the default description value of the property, for new products in the group. |
|Default_Value_Id|`Guid?`||When not null, specifies the default internal Id value of the property, for new products in the group. `Filter(multi eq)` |
|Property_No|`Int32`||The consecutive number (position) of the property within the product group and its subgroups. The parent groups of each leaf group should contain only unique property numbers. `Required` `Default(0)` |
|Required|`Boolean`||Specifies whether the property is required (or only suggested) to be set for new products. Suggested properties are used by product configuration and other product creation services. true=Required, false=Suggested. `Required` `Default(false)` |
