# Table Sec_Groups

Groups of users. Used for providing group access to secured data. Entity: Sec_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Group_Id|`Guid`|`PK`, Readonly||
|Edit_Period_Days|`Int32?`||The number of days before which the documents can not be corrected, released or voided. |
|Group_Type|`GroupType`|Allowed: `G`, `U`, `A`, `E`, Readonly|Group type. G=Normal user-definable group; U=System group for 1 user; A=Admin; E=Everybody. `Required` `Default("G")` `ReadOnly` |
|Group_Name|`MultilanguageString`||The name of this Group. `Required` `Filter(like)` `ORD` |
|Notes|`String`||Notes for this Group. |
