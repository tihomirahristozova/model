# Table Gen_Property_Allowed_Values

User-defined properties allowed values. Can be specified only for properties with unbound allowed values (e.g. for which Allowed Values Entity is not set). Entity: Gen_Property_Allowed_Values

# Aggregate Hierarchy

* [Gen_Properties](Gen_Properties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Property_Allowed_Value_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||Specifies whether the allowed value is active and can be used when selecting property values. `Required` `Default(true)` `Filter(eq)` |
|Description|`MultilanguageString`||The description of the property allowed value. Used to fill the Description column of the Property_Value in Gen_Property_Values_Table. `Filter(eq;like)` |
|Long_Description|`String`||When not null, specifies a long description of the allowed value. This long description is only used as helper information when selecting values, it is not copied in the property value. |
|Parent_Allowed_Value_Id|`Guid?`||The value of the parent property, for which this allowed value is valid. `Filter(multi eq)` |
|Picture|`Byte[]`|`BLOB`|When not null, specifies a picture representation of the allowed value. |
|Property_Allowed_Value|`String`||The actual allowed value. `Required` `Filter(eq;like)` |
