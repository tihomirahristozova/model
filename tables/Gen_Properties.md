# Table Gen_Properties

User-defined properties, which can supplement the system properties of almost all entities in the system. Entity: Gen_Properties

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Property_Id|`Guid`|`PK`, Readonly||
|Allowed_Values_Entity_Name|`String`||When not null, specifies that the allowed values are retrieved from the specified entity. `Filter(eq)` |
|Allowed_Values_Filter_XML|`String`||When not null specifies the filter to apply when extracting allowed values from entity. |
|Property_Code|`String`||Unique property code. `Required` `Filter(multi eq;like)` `ORD` |
|Entity_Name|`String`||The entity for which the property is applicable. `Required` `Filter(eq)` `ORD` |
|Hint|`MultilanguageString`||The hint, which is displayed alongside the property. `Filter(multi eq;like)` `Introduced in version 20.1` |
|Key_Order|`Byte?`||When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis. |
|Limit_To_Allowed_Values|`Boolean`||When true, allows the property to be set only to allowed value. When false, the property can have any value. `Required` `Default(false)` `Filter(eq)` |
|Mask_Length|`Int16?`||Limits te length of the property value to the specified number of characters. Null means no limitation. |
|Property_Name|`MultilanguageString`||The name of this CustomProperty. `Required` `Filter(like)` `ORD` |
|Notes|`String`||Notes for this CustomProperty. `Introduced in version 20.1` |
|Property_Type|`PropertyType`|Allowed: `T`, `N`, `P`, `D`|Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date. `Required` `Default("T")` |
