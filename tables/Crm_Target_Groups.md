# Table Crm_Target_Groups

Marketing target group, containing a fixed list of parties. Entity: Crm_Target_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Target_Group_Id|`Guid`|`PK`, Readonly||
|Target_Group_Code|`String`||Short code for identification of target groups. `Required` `Filter(eq;like)` `ORD` |
|Description|`String`||The description of this TargetGroup. |
|Target_Group_Name|`String`||The name of this TargetGroup. `Required` `Filter(like)` |
