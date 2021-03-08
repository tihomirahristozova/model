# Table Gen_Property_Values

The actual values of the user-defined properties for each actual entity. Entity: Gen_Property_Values

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Property_Value_Id|`Guid`|`PK`, Readonly||
|Description|`MultilanguageString`||The actual description value of the property for the specified entity (the entity with the specified Id). |
|Entity_Item_Id|`Guid`||The Id of the actual entity for which the value is specified. `Required` `Filter(multi eq)` |
|Picture|`Byte[]`|`BLOB`|The actual picture of the property for the specified entity (the entity with the specified Id). |
|Property_Value|`String`||The actual value of the property for the specified entity (the entity with the specified Id). |
|Value_Id|`Guid?`||The internal Id of the value of the property for the specified entity (the entity with the specified Id). For choosable properties, this contains the id of the original "allowed value" row, from which the value was derived. null for non-choosable (free-text) properties, but also for old property values (before this id was available) or other unknown values. `Filter(multi eq)` |
