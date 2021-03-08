# Table Fleet_Crew_Members

Contains the memnbers of vehicle crews. Entity: Fleet_Crew_Members

# Aggregate Hierarchy

* [Fleet_Crews](Fleet_Crews.md)
* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Crew_Member_Id|`Guid`|`PK`, Readonly||
|Notes|`String`||Notes for this CrewMember. |
|Ordinal_Pos|`Int32?`||Ordinal position. Ordinal_Pos=0 has special meaning - this is the crew leader. |
