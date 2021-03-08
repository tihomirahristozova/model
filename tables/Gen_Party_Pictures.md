# Table Gen_Party_Pictures

Party pictures - photos, logos, etc. Entity: Gen_Party_Pictures

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Party_Picture_Id|`Guid`|`PK`, Readonly||
|Comments|`String`||Notes for this party picture. |
|Is_Default|`Boolean`||True=This is the default picture for the party; false=otherwise. `Required` `Default(false)` `Filter(eq)` |
|Is_Logo|`Boolean`||If checked specifies that this picture is used to visualize the logo of this party in the system. `Required` `Default(false)` `Filter(eq)` |
|Picture|`Byte[]`|`BLOB`|The actual party picture data. Can be null if we insert only some comments. |
|Picture_No|`Int32`||Unique picture number within the party. Also used for sorting. `Required` `Filter(eq)` |
