# Table Cm_Party_Contact_Mechanisms

Specifies the contact mechanisms, which are attached to the parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Party_Contact_Mechanisms

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|From_Date|`DateTime?`||The first date when the contact mechanism was valid. null means unknown date. `Default(Today)` `Filter(eq;ge;le)` |
|Is_Active|`Boolean`||True if the contact mechanism is currently active and can be used to contact the party. `Required` `Default(true)` `Filter(eq)` |
|Is_Default|`Boolean`||True - when this is the default contact mechanism for this party; false - otherwise. `Required` `Default(false)` `Filter(eq)` |
|Line_Ord|`Int32`||Consecutive number of the contact information. The number is unique within the party. `Required` |
|Non_Solicitation|`Boolean`||If true then Don't use the mechanism for solicitation purposes. `Required` `Default(false)` `Filter(eq)` |
|Notes|`String`||Notes for this PartyContactMechanism. |
|Thru_Date|`DateTime?`||The last date on which the contact mechanism was valid for the party. null if the contact mechanism is still valid. `Filter(eq;ge;le)` |
