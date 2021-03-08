# Table Wf_Routes

Contains document routes, which specify which document generation procedures will be run upon document events. Entity: Wf_Routes

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Route_Id|`Guid`|`PK`, Readonly||
|Activation_Date|`DateTime`||The date from which (including) the route is active. The date is matched against the document date of the generating document. `Required` `Default(Today)` `Filter(ge;le)` |
|Active|`Boolean`||True if the route is active, otherwise false. `Required` `Default(true)` `Filter(eq)` |
|Allowed_Generation_Types|`AllowedGenerationTypes`|Allowed: `A`, `B`, `M`|Determines the possible types of the generation of the destination document: A=Auto, M=Manual, B=Both (Auto and Manual). `Required` `Default("B")` `Filter(multi eq)` |
|Allow_Obsolete_Generation|`Boolean`||Allows the usage of unsupported generation procedures (marked as obsolete). This is a user override of the system prohibition of the usage of obsolete procedures. `Required` `Default(false)` |
|Condition_Filter_XML|`DataAccessFilter`||Contains filter condition, which the document must match in order to execute the route. |
|Condition_States_Bit_Mask|`DocumentStateFlags`|Allowed (flags): `1`, `2`, `4`, `8`, `16`, `32`, `64`|The system states for which to execute the specified route. `Required` `Default(0)` |
|Connected_Party_Condition|`ConnectedPartyCondition`|Allowed: `A`, `C`, `U`|A - any party; C - connected party: to_party is enterprise company; U - unconnected party - not enterprise company;. `Required` `Default("A")` |
|Deactivation_Date|`DateTime?`||The date until (including) the route is active. The date is matched against the document date of the generating document. Null means the route does not have a deactivation date. `Filter(ge;le)` |
|Destination_State|`DocumentState`|Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`|0=New;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed. `Required` |
|Negative_Condition_Filter_Xml|`DataAccessFilter`||The negative condition should NOT be matched by the document in order to execute the route. |
|Notes|`String`||Notes for this Route. |
|Parent_Document_Relationship_Type|`ParentDocumentRelationshipType`|Allowed: `S`, `N`|Determines the default relationship type between the generated document and the parent document. `Required` `Default("S")` |
|Procedure_Name|`String`||The system name of the generation procedure, which must be executed by the route. `Required` |
|Process_Event|`String`||Event which triggers the route. Usually the event is change of state. Every document entity may define own custom events. `Required` |
|Read_Only|`Boolean`||Indicates wheather the destination document shoul be read only. true - the destination document is read only. `Required` `Default(false)` |
