# Table Acc_Account_Groups

Hierarchical chart of account groups. Entity: Acc_Account_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Account_Group_Id|`Guid`|`PK`, Readonly||
|Description|`MultilanguageString`||The description of this AccountGroup. |
|Discontinued|`Boolean`||True means that the account group won't be used any more and should not appear in combo boxes. `Required` `Default(false)` `Filter(eq)` |
|Full_Path|`String`||Full path to the group. Contains delimited list of group numbers of parent groups. `Filter(like)` |
|Account_Group_Name|`MultilanguageString`||Account group name, required. Must be unique within the parent group. `Required` `Filter(like)` |
|Account_Group_Number|`String`||Unique account group number. May contain characters, if required. `Required` `Filter(like)` `ORD` |
