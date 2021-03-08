# Table Cm_Party_Relationships

Defines the relationships between the parties. The data is preserved over time. Entity: Cm_Party_Relationships

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Relationship_Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||The starting date of the relationship. null means the date is the begining of the time. `Filter(ge;le)` |
|Notes|`String`||Notes for this PartyRelationship. |
|To_Date|`DateTime?`||The ending date of the relationship. null means the relationship is still active. `Filter(ge;le)` |
